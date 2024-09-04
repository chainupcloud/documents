---
description: The Transfers API allows you to easily fetch historical transactions
---

# Transfer API

<mark style="color:blue;">`GET`</mark> `/nft/{chain}/{token}/getAssetsTransfer` &#x20;

#### Path Parameters

| Name                                      | Type   | Description                                                                      |
| ----------------------------------------- | ------ | -------------------------------------------------------------------------------- |
| {chain}<mark style="color:red;">\*</mark> | String | Placeholder for the blockchain identifier (e.g., Ethereum, Binance Smart Chain). |
| token<mark style="color:red;">\*</mark>   | String | Placeholder for the NFT token identifier.                                        |

{% tabs %}
{% tab title="Scroll" %}
{% code overflow="wrap" %}
```
curl -X POST "https://nft.chainup.net/scroll_mainnet/token/v1/getAssetTransfers" --data '{"category": ["ERC721"],"max_count": 5}' | jq .
```
{% endcode %}
{% endtab %}

{% tab title="HoleSky" %}
{% code overflow="wrap" %}
```
curl -X POST "https://nft.chainup.net/eth_holesky/token/v1/getAssetTransfers" --data '{"category": ["ERC721"],"max_count": 5}' | jq .
```
{% endcode %}
{% endtab %}
{% endtabs %}
