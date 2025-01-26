---
description: >-
  Protect your crypto! Install the Quick Intel Snap for MetaMask and get
  real-time token audit reports while swapping.
---

# Introduction

## MetaMask Snap - Quick Intel Token Audit

The Quick Intel Snap is a revolutionary add-on to the popular MetaMask wallet!\
\
With the MetaMask Snap, users can now access a quick token audit when interacting with DEXs and swapping for tokens.&#x20;

\
The MetaMask Snap gives users a quick overview of potential risks within the smart contract, so they can better stay protected BEFORE investing and potentially avoiding scams and rug pulls.\


The Quick Intel Snap installation is extremely simple and takes just a few seconds. <mark style="color:yellow;">You can install the Snap through either of these methods:</mark>

* Go to the MetaMask Quick Intel Snap directory: [Quick Intel MetaMask Snap Page](https://snaps.metamask.io/snap/npm/quickintel/quickintel-snap/)
* Visit the Quick Intel Snap page on our website: [https://quickintel.io/snap](https://quickintel.io/snap)

{% embed url="https://framerusercontent.com/assets/2xbCgtIAx5SuwASd0Kj40FzdQI.mp4" %}

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption><p>Quick Intel Snap</p></figcaption></figure>

### How is this done?

With the Quick Intel Snap, every time a user initiates a transaction, the Quick Intel Snap API is invoked. The Chain ID and transaction data are sent via a POST request.\
\
Quick Intel then grabs that transaction data and decompiles it, extracting the token(s) being interacted with in the request.\
\
Once the token(s) are extracted, an audit is performed, and the results are returned via an array to the Quick Intel Snap.\
\
Due to how Quick Intel extracts the token(s), the Quick Intel Snaps supports any DEX on any of the supported chains, providing the user with the best user experience, ease of use, and minimal complexity.\
\
The results are then displayed to the user via the Quick Intel Snap, and in the event of multi-token interactions/swaps, an audit for each token is returned.
