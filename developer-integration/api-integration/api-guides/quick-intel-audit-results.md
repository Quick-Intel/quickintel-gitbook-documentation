---
description: >-
  The Quick Intel API full audit endpoint returns a lot of information.  If you
  don't need all of that information, the Quick Audit endpoint may be exactly
  what you are after.
---

# Quick Intel Audit - Results

### Quick Intel Audit Results

Let's walk through the results of the Quick Intel Audit to ensure you have an understanding of how to read the data.

The Audit result has 3 key sections.

<figure><img src="../../../../.gitbook/assets/image (81).png" alt=""><figcaption><p>Results</p></figcaption></figure>

1. Token Details - Will return token information along with the token owner if there is one.
2. Contract Verified - This will state if the contract is verified.
3. Quick Intel Audit - This section outlines all of the audited results.

### Quick Intel Audit In-Depth

Most items in the Quick Intel Audit are self-explanatory, but let's dive into a few areas to ensure a clear understanding.

1.  Let's look at the items "**can\_Blacklist**" and "**cant\_Blacklist\_Renounced**".



    <figure><img src="../../../../.gitbook/assets/image (83).png" alt=""><figcaption><p>Result 1</p></figcaption></figure>

    Although they sound similar, they serve different purposes.

    * **"can\_Blacklist"** means the ability to perform this action is there.
    * **"cant\_Blacklist\_Renounced"** means that IF/WHEN the contract is renounced, they can no longer run the above action. If this were false, while the **"can\_Blacklist"** was true, that would mean that IF/WHEN the contract gets renounced, the ability to perform this action is still there EVEN if it is renounced.

### **External, Suspicious, and Scam Functions**

<figure><img src="../../../../.gitbook/assets/image (86).png" alt=""><figcaption><p>Result 2</p></figcaption></figure>

1. **Suspicious Functions** refer to actions within the contract that may not be "normal".  This does not constitute any action to be good or bad but is advised to review.
2. **External Functions** are actions that can be run **EVEN** when the contract has been renounced.
3. **Audit Functions** are functions related to the modification of taxes
4. **Scam Functions** are known scams that are tracked by Quick Intel. This will return the matched scam, along with the scam data, when there is a match.

### Additional Data

<figure><img src="../../../../.gitbook/assets/image (87).png" alt=""><figcaption><p>Result 3</p></figcaption></figure>

1. **Contract Links** are links that have been embedded within the smart contract.
2. **Functions** is the list of WRITE functions that are available.
3. **Only Owner Functions** is the list of functions that are controlled via the "onlyOwner" modifier.
4. **Multi-Blacklist Functions** are potential actions that can be used to multi-blacklist wallets.
