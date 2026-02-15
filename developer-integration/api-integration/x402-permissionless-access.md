---
icon: lock-open
---

# x402 Permissionless Access

x402 Permissionless Access

### Overview

Access Quick Intel's token scanning API **without API keys or registration**. Pay $0.03 per scan with USDC using the x402 protocol.

**Best for:**

* AI agents and autonomous systems
* Developers who want instant access
* Pay-as-you-go usage without commitments

***

### Pricing

| Endpoint   | Price              |
| ---------- | ------------------ |
| Token Scan | **$0.03 per call** |

Paid in **USDC** on any supported chain (Base recommended for lowest fees).

***

### Endpoint

```
POST https://x402.quickintel.io/v1/scan/full
```

#### Request Body

```json
{
  "chain": "base",
  "tokenAddress": "0x4ed4e862860bed51a9570b96d89af5e1b0efefed"
}
```

| Field          | Type   | Required | Description                                       |
| -------------- | ------ | -------- | ------------------------------------------------- |
| `chain`        | string | ✅        | Chain name (e.g., "base", "ethereum", "arbitrum") |
| `tokenAddress` | string | ✅        | Token contract address                            |

#### Response

Same response format as the standard API — full token security analysis including honeypot detection, tax analysis, ownership status, and risk scoring.

***

### How It Works

#### 1. Make Request (Get 402)

```bash
curl -X POST https://x402.quickintel.io/v1/scan/full \
  -H "Content-Type: application/json" \
  -d '{
    "chain": "base",
    "tokenAddress": "0x4ed4e862860bed51a9570b96d89af5e1b0efefed"
  }'
```

**Response:** `402 Payment Required` with payment instructions in `PAYMENT-REQUIRED` header.

#### 2. Sign Payment

Sign an EIP-712 `TransferWithAuthorization` message authorizing $0.03 USDC transfer.

```javascript
const authorization = {
  from: walletAddress,
  to: paymentInfo.payTo,
  value: "30000",  // $0.03 USDC (6 decimals)
  validAfter: 0,
  validBefore: Math.floor(Date.now() / 1000) + 3600,
  nonce: randomBytes32()
};

const signature = await wallet.signTypedData({
  domain: {
    name: "USD Coin",
    version: "2",
    chainId: 8453,
    verifyingContract: "0x833589fCD6eDb6E08f4c7C32D4f71b54bdA02913"
  },
  types: {
    TransferWithAuthorization: [
      { name: "from", type: "address" },
      { name: "to", type: "address" },
      { name: "value", type: "uint256" },
      { name: "validAfter", type: "uint256" },
      { name: "validBefore", type: "uint256" },
      { name: "nonce", type: "bytes32" }
    ]
  },
  primaryType: "TransferWithAuthorization",
  message: authorization
});
```

#### 3. Retry with Payment Header

```bash
curl -X POST https://x402.quickintel.io/v1/scan/full \
  -H "Content-Type: application/json" \
  -H "PAYMENT-SIGNATURE: " \
  -d '{
    "chain": "base",
    "tokenAddress": "0x4ed4e862860bed51a9570b96d89af5e1b0efefed"
  }'
```

**Response:** `200 OK` with full token scan results.

***

### Supported Payment Networks

| Chain     | Token | Chain ID |
| --------- | ----- | -------- |
| Base      | USDC  | 8453     |
| Ethereum  | USDC  | 1        |
| Arbitrum  | USDC  | 42161    |
| Optimism  | USDC  | 10       |
| Polygon   | USDC  | 137      |
| Avalanche | USDC  | 43114    |
| MegaETH   | USDM  | 4326     |

**Recommended:** Use **Base** for lowest gas fees.

***

### Quick Example

```javascript
import { privateKeyToAccount } from 'viem/accounts';
import { keccak256, toHex } from 'viem';

const GATEWAY_URL = 'https://x402.quickintel.io';
const account = privateKeyToAccount(process.env.PRIVATE_KEY);

async function scanToken(chain, tokenAddress) {
  // 1. Get 402 response
  const initial = await fetch(`${GATEWAY_URL}/v1/scan/full`, {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify({ chain, tokenAddress })
  });
  
  const { paymentRequired } = await initial.json();
  const paymentInfo = paymentRequired.accepts.find(a => a.network === 'eip155:8453');
  
  // 2. Sign payment
  const nonce = keccak256(toHex(`${Date.now()}-${Math.random()}`));
  const validBefore = BigInt(Math.floor(Date.now() / 1000) + 3600);
  
  const signature = await account.signTypedData({
    domain: {
      name: paymentInfo.extra.name,
      version: paymentInfo.extra.version,
      chainId: 8453,
      verifyingContract: paymentInfo.asset
    },
    types: {
      TransferWithAuthorization: [
        { name: 'from', type: 'address' },
        { name: 'to', type: 'address' },
        { name: 'value', type: 'uint256' },
        { name: 'validAfter', type: 'uint256' },
        { name: 'validBefore', type: 'uint256' },
        { name: 'nonce', type: 'bytes32' }
      ]
    },
    primaryType: 'TransferWithAuthorization',
    message: {
      from: account.address,
      to: paymentInfo.payTo,
      value: BigInt(paymentInfo.maxAmountRequired),
      validAfter: 0n,
      validBefore,
      nonce
    }
  });
  
  const paymentPayload = btoa(JSON.stringify({
    x402Version: 2,
    scheme: 'exact',
    network: 'eip155:8453',
    payload: {
      signature,
      authorization: {
        from: account.address,
        to: paymentInfo.payTo,
        value: paymentInfo.maxAmountRequired,
        validAfter: '0',
        validBefore: validBefore.toString(),
        nonce
      }
    }
  }));
  
  // 3. Retry with payment
  const response = await fetch(`${GATEWAY_URL}/v1/scan/full`, {
    method: 'POST',
    headers: {
      'Content-Type': 'application/json',
      'PAYMENT-SIGNATURE': paymentPayload
    },
    body: JSON.stringify({ chain, tokenAddress })
  });
  
  return response.json();
}

// Usage
const result = await scanToken('base', '0x4ed4e862860bed51a9570b96d89af5e1b0efefed');
console.log(result);
```

***

### x402 vs API Key

| Feature        | API Key                        | x402                     |
| -------------- | ------------------------------ | ------------------------ |
| Registration   | Required                       | None                     |
| Authentication | API key header                 | USDC payment             |
| Pricing        | Subscription/credits           | $0.03 per call           |
| Rate limits    | Per plan                       | Unlimited                |
| Best for       | High volume, predictable usage | AI agents, pay-as-you-go |

***

### Learn More

* [x402 Protocol](https://x402.org) — Protocol specification
