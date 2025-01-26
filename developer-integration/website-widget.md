---
description: >-
  Want to integrate Quick Intel Security Scanner directly into your dApp?  We
  have you covered!  Read below on how to use the Quick Intel Scanner Widget.
---

# Website Widget

Quick intel has a widget that anyone can integrate into their site, like a dApp, DEX, etc.

Integrating the Quick Intel widget will allow users to get a quick overview of any token across any chain we support.

For a list of supported chains please see the below page.

{% content-ref url="api-integration/supported-chains-and-dex.md" %}
[supported-chains-and-dex.md](api-integration/supported-chains-and-dex.md)
{% endcontent-ref %}

Simply add an iFrame into your location, with pre-set parameters.

| Parameter       | Values                                      |
| --------------- | ------------------------------------------- |
| widget          | true or false                               |
| widgetView      | slim or wide                                |
| type            | token                                       |
| chain           | chain of token to be scaned (eth, bsc, etc) |
| contractAddress | address of token                            |

Example URL with both a slim and wide option of the chart.\
\
**Slim View**

\
URL: https://app.quickintel.io/widget?widget=true\&widgetView=slim\&type=token\&chain=arbitrum\&contractAddress=0x6d038130b9b379a373b1d33a29d5904ed1bb9026

<figure><img src="../.gitbook/assets/image (90).png" alt=""><figcaption><p>Slim Widget</p></figcaption></figure>

**Wide View**

\
URL: https://app.quickintel.io/widget?widget=true\&widgetView=wide\&type=token\&chain=arbitrum\&contractAddress=0x6d038130b9b379a373b1d33a29d5904ed1bb9026

<figure><img src="../.gitbook/assets/image (91).png" alt=""><figcaption><p>Wide Widget</p></figcaption></figure>
