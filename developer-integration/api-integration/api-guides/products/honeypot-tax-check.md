# Honeypot/Tax Check

Honeypot/Tax Check

Select "Endpoints" and expand the "Honeypot" to view the parameters required for the request.

<figure><img src="../../../../.gitbook/assets/image (98).png" alt=""><figcaption></figcaption></figure>

After selecting the endpoint, you will see the requirements, along with the ability to try it out directly from the browser.

<figure><img src="../../../../.gitbook/assets/image (99).png" alt=""><figcaption></figcaption></figure>

1. This will be the full URL endpoint to leverage along with the type of request (GET, POST, etc)
2. This outlines the data needed to make the request.
   1. dex- The dex from the list of supported dexes by Quick Intel.
   2. token- The contract address for the token you are performing an audit on.
   3. lptoken - The contract for the paired token.  Use "default" to scan against the native chain token (IE. WETH, WBNB, etc). If you want to scan against USDT, USDC, replace "default" with the contract address of the paired token
3. The try it out button lets you test the request directly from the browser.
