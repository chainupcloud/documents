---
description: The Transfers API allows you to easily fetch historical transactions
---

# Transfer API

{% swagger method="get" path="" baseUrl="/nft/{chain}/{token}/getAssetsTransfer  " summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="{chain}" required="true" %}
Placeholder for the blockchain identifier (e.g., Ethereum, Binance Smart Chain).
{% endswagger-parameter %}

{% swagger-parameter in="path" name="token" required="true" %}
Placeholder for the NFT token identifier.
{% endswagger-parameter %}
{% endswagger %}

{% tabs %}
{% tab title="Scroll" %}
{% code overflow="wrap" %}
```
curl -X POST "https://nft.chainup.net/scroll_mainnet/{token}/v1/getAssetTransfers" --data '{"category": ["ERC721"],"max_count": 5}'
```
{% endcode %}
{% endtab %}

{% tab title="HoleSky" %}
{% code overflow="wrap" %}
```
curl -X POST "https://nft.chainup.net/eth_holesky/{token}/v1/getAssetTransfers" --data '{"category": ["ERC721"],"max_count": 5}'
```
{% endcode %}
{% endtab %}
{% endtabs %}
