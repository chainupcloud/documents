# NFT Metadata Access



## Gets the metadata associated with a given Contract.

<mark style="color:blue;">`GET`</mark> `GET/nft/{chain}/{token}/getContractMetadata`&#x20;

{% tabs %}
{% tab title="Scroll" %}
{% code overflow="wrap" %}
```
curl "http://nft.chainup.net/scroll_mainnet/token/v1/getOwnersForNFT?token_id={TOKEN_ID}&contract_address={CONTRACT_ADDRESS}"
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



## Gets the metadata associated with a given Contract.

<mark style="color:blue;">`GET`</mark> `/nft/{chain}/{token}/getContractMetadataBatch`      &#x20;

{% tabs %}
{% tab title="Scroll" %}
{% code overflow="wrap" %}
```
curl -X POST "http://nft.chainup.net/scroll_mainnet/token/v1/getContractMetadataBatch" --data '{"contract_addresses": ["{CONTRACT_ADDRESSES_1}", "{CONTRACT_ADDRESSES_2}" ]}'
```
{% endcode %}
{% endtab %}

{% tab title="HoleSky" %}
{% code overflow="wrap" %}
```
curl -X POST "http://nft.chainup.net/eth_holesky/token/v1/getContractMetadataBatch" --data '{"contract_addresses": ["{CONTRACT_ADDRESSES_1}", "{CONTRACT_ADDRESSES_2}" ]}'
```
{% endcode %}
{% endtab %}
{% endtabs %}



## Gets the metadata associated with a given NFT.

<mark style="color:blue;">`GET`</mark> `/nft/{chain}/{token}/getNFTMetadata`          &#x20;

{% tabs %}
{% tab title="Scroll" %}
{% code overflow="wrap" %}
```
curl "http://nft.chainup.net/scroll_mainnet/token/v1/getNFTMetadata?contract_address={CONTRACT_ADDRESSES_1}&token_id={TOKEN_ID}&token_type=ERC721"
```
{% endcode %}
{% endtab %}

{% tab title="HoleSky" %}
{% code overflow="wrap" %}
```
curl "http://nft.chainup.net/eth_holesky/token/v1/getNFTMetadata?contract_address={CONTRACT_ADDRESSES_1}&token_id={TOKEN_ID}&token_type=ERC721"
```
{% endcode %}
{% endtab %}
{% endtabs %}



## Gets the metadata associated with a given NFT.&#x20;

<mark style="color:green;">`POST`</mark> `/nft/{chain}/{token}/getNFTMetadataBatch`

{% tabs %}
{% tab title="Scroll" %}
{% code overflow="wrap" %}
```
curl -X POST "http://nft.chainup.net/scroll_mainnet/token/v1/getNFTMetadataBatch" --data '{"tokens":[{"contract_address": "{CONTRACT_ADDRESSES_1}", "token_id": {TOKEN_ID} }]}'
```
{% endcode %}
{% endtab %}

{% tab title="HoleSky" %}
{% code overflow="wrap" %}
```
curl -X POST "http://nft.chainup.net/eth_holesky/token/v1/getNFTMetadataBatch" --data '{"tokens":[{"contract_address": "{CONTRACT_ADDRESSES_1}", "token_id": {TOKEN_ID} }]}'
```
{% endcode %}
{% endtab %}
{% endtabs %}



## Gets the metadata associated with a given Contract.&#x20;

<mark style="color:blue;">`GET`</mark> `/nft/{chain}/{token}/searchContractMetadata`

{% tabs %}
{% tab title="Scroll" %}
{% code overflow="wrap" %}
```
curl -X GET "http://nft.chainup.net/scroll_mainnet/token/v1/searchContractMetadata?query=Meme"
```
{% endcode %}
{% endtab %}

{% tab title="HoleSky" %}
{% code overflow="wrap" %}
```
curl -X GET "http://nft.chainup.net/eth_holesky/token/v1/searchContractMetadata?query=Meme"
```
{% endcode %}
{% endtab %}
{% endtabs %}
