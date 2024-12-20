# MetaMask Wallet Connect

This article describes the steps needed when you are having issues connecting your MetaMask wallet to the Quick Intel Web and Mobile apps.

{% hint style="info" %}
MetaMask connection issues can sometimes occur when you do not complete the read-only transaction signing process, which validates your wallet. It is a known issue but is fairly easy to resolve.
{% endhint %}

### 📘  Instructions <a href="#metamaskwallettroubleshooting-instructions" id="metamaskwallettroubleshooting-instructions"></a>

Let’s walk you through some steps to see if MetaMask is simply waiting for you to approve the signing:

1. Go into MetaMask (mobile app or web extension as appropriate)
2. On the connected wallet, click on "Activity."
   1.  If you see just one [app.quickintel.io](http://app.quickintel.io/) unapproved request, click it and sign (**you should now be connected**)



       <figure><img src="https://quickintel.atlassian.net/plugins/servlet/servicedesk/customer/confluence/shim/download/thumbnails/12583038/K7pQYoT-PAjsPPTkVU9h57vbNI0aq5J81fFNYocsV2juMD5yRfLj8q3mQ7nlBv1eJB8ByM4a55BMvwAkWDkcAbneeRmSSeVH3dkqx52-30OP8sc7VhqBna-MkRQBDrqVBgZxVMxHBZFqrjbz0DgaNbA?version=2&#x26;modificationDate=1700352419033&#x26;cacheVersion=1&#x26;api=v2&#x26;width=250&#x26;height=36" alt=""><figcaption></figcaption></figure>
   2. If you see multiple unapproved requests:
      1.  Click on the **bottom** "Signature request" (where it says unapproved), and it will open up a signature request message



          <figure><img src="https://quickintel.atlassian.net/plugins/servlet/servicedesk/customer/confluence/shim/download/thumbnails/12583038/SDh24UyuzVTqnMerb9cAiGEV3WkdXWqXx0BGYeHkjdpDvBAY3Z9IZrgz2hlqUPsG61JHiyBmu3_JaIxj8RwUZJb95z2PKzQ00oyfeNzgQ38EPlx4aA35sxC8x8fuu71443gjAIpmaXb_J9ZbMmTFzWY?version=1&#x26;modificationDate=1700352419011&#x26;cacheVersion=1&#x26;api=v2&#x26;width=250&#x26;height=55" alt=""><figcaption></figcaption></figure>
      2.  Click "Reject"



          <figure><img src="https://quickintel.atlassian.net/plugins/servlet/servicedesk/customer/confluence/shim/download/thumbnails/12583038/JRwKqG3e7min44oZjHpmO7R3hy7tEYb3NOrwqqn47-1rZhmcKxWzOlm-eYMxHOrg9eObk8Lf8Sx7bIeR42PSg4QKiWAZTjH0pTNPzNKQ_3msPHxEbBXZMckRGyW9djNwj-94B3cAzL_GeeeMSz2yp1w?version=1&#x26;modificationDate=1700352419017&#x26;cacheVersion=1&#x26;api=v2&#x26;width=250&#x26;height=91" alt=""><figcaption></figcaption></figure>
      3.  Continue rejecting the unapproved requests till there is just one [app.quickintel.io](http://app.quickintel.io/) request remaining



          <figure><img src="https://quickintel.atlassian.net/plugins/servlet/servicedesk/customer/confluence/shim/download/thumbnails/12583038/K7pQYoT-PAjsPPTkVU9h57vbNI0aq5J81fFNYocsV2juMD5yRfLj8q3mQ7nlBv1eJB8ByM4a55BMvwAkWDkcAbneeRmSSeVH3dkqx52-30OP8sc7VhqBna-MkRQBDrqVBgZxVMxHBZFqrjbz0DgaNbA?version=2&#x26;modificationDate=1700352419033&#x26;cacheVersion=1&#x26;api=v2&#x26;width=250&#x26;height=36" alt=""><figcaption></figcaption></figure>
      4. Click the last remaining unapproved request and then sign
         1. If the issue is not resolved, then reject that one as well and attempt reconnecting
