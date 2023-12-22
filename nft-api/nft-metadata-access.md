# NFT Metadata Access



{% swagger method="get" path="" baseUrl="GET/nft/{chain}/{token}/getContractMetadata " summary="Gets the metadata associated with a given Contract." %}
{% swagger-description %}

{% endswagger-description %}
{% endswagger %}

a

{% tabs %}
{% tab title="Scroll" %}
{% code overflow="wrap" %}
```
curl "http://nft.chainup.net/scroll_mainnet/token/v1/getOwnersForNFT?token_id={TOKEN_ID}&contract_address={CONTRACT_ADDRESS}
```
{% endcode %}
{% endtab %}

{% tab title="HoleSky" %}
```
curl -X POST "https://nft.chainup.net/eth_holesky/{token}/v1/getAssetTransfers"\
--data '{"category": ["ERC721"],"max_count": 5}'
```
{% endtab %}
{% endtabs %}

a



{% swagger method="get" path="" baseUrl="/nft/{chain}/{token}/getContractMetadataBatch       " summary="Gets the metadata associated with a given Contract." %}
{% swagger-description %}

{% endswagger-description %}
{% endswagger %}





{% swagger method="get" path="" baseUrl="/nft/{chain}/{token}/getNFTMetadata           " summary="Gets the metadata associated with a given NFT." %}
{% swagger-description %}

{% endswagger-description %}
{% endswagger %}



{% swagger method="post" path="" baseUrl="/nft/{chain}/{token}/getNFTMetadataBatch" summary="Gets the metadata associated with a given NFT. " %}
{% swagger-description %}

{% endswagger-description %}
{% endswagger %}



{% swagger method="get" path="" baseUrl="/nft/{chain}/{token}/searchContractMetadata" summary="Gets the metadata associated with a given Contract. " %}
{% swagger-description %}

{% endswagger-description %}
{% endswagger %}

