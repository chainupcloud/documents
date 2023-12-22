# Ownership & Token Gating

{% swagger method="get" path="    " baseUrl="/nft/{chain}/{token}/getContractsForOwner  " summary="" %}
{% swagger-description %}

{% endswagger-description %}
{% endswagger %}

{% tabs %}
{% tab title="Scroll" %}
{% code overflow="wrap" %}
```
curl "http://nft.chainup.net/scroll_mainnet/token/v1/getContractsForOwner?owner={OWNER_ADDRESS}"
```
{% endcode %}
{% endtab %}

{% tab title="HoleSky" %}
{% code overflow="wrap" %}
```
curl "http://nft.chainup.net/eth_holesky/token/v1/getContractsForOwner?owner={OWNER_ADDRESS}"
```
{% endcode %}
{% endtab %}
{% endtabs %}



{% swagger method="get" path="" baseUrl="/nft/{chain}/{token}/getNFTsForOwner              " summary="" %}
{% swagger-description %}

{% endswagger-description %}
{% endswagger %}

{% tabs %}
{% tab title="Scroll" %}
{% code overflow="wrap" %}
```
curl "http://nft.chainup.net/scroll_mainnet/token/v1/getNFTsForOwner?owner={OWNER_ADDRESS}&contract_addresses={CONTRACT_ADDRESS}"
```
{% endcode %}
{% endtab %}

{% tab title="HoleSky" %}
{% code overflow="wrap" %}
```
curl "http://nft.chainup.net/eth_holesky/token/v1/getNFTsForOwner?owner={OWNER_ADDRESS}&contract_addresses={CONTRACT_ADDRESS}"
```
{% endcode %}
{% endtab %}
{% endtabs %}



{% swagger method="get" path="            " baseUrl="/nft/{chain}/{token}/getOwnersForContract" summary="" %}
{% swagger-description %}

{% endswagger-description %}
{% endswagger %}

{% tabs %}
{% tab title="Scroll" %}
{% code overflow="wrap" %}
```
curl "http://nft.chainup.net/scroll_mainnet/token/v1/getOwnersForContract?contract_address={CONTRACT_ADDRESS}"
```
{% endcode %}
{% endtab %}

{% tab title="HoleSky" %}
{% code overflow="wrap" %}
```
curl "http://nft.chainup.net/eth_holesky/token/v1/getOwnersForContract?contract_address={CONTRACT_ADDRESS}"
```
{% endcode %}
{% endtab %}
{% endtabs %}







{% swagger method="get" path="" baseUrl="/nft/{chain}/{token}/getOwnersForNFT            " summary="" %}
{% swagger-description %}

{% endswagger-description %}
{% endswagger %}

{% tabs %}
{% tab title="Scroll" %}
{% code overflow="wrap" %}
```
curl "http://nft.chainup.net/scroll_mainnet/token/v1/getOwnersForNFT?token_id={TOKEN_ID}&contract_address={CONTRACT_ADDRESS}"
```
{% endcode %}
{% endtab %}

{% tab title="HoleSky" %}
{% code overflow="wrap" %}
```
curl "http://nft.chainup.net/eth_holesky/token/v1/getOwnersForNFT?token_id={TOKEN_ID}&contract_address={CONTRACT_ADDRESS}"
```
{% endcode %}
{% endtab %}
{% endtabs %}



{% swagger method="get" path="" baseUrl="/nft/{chain}/{token}/isHolderOfContract " summary="" %}
{% swagger-description %}

{% endswagger-description %}
{% endswagger %}

{% tabs %}
{% tab title="Scroll" %}
{% code overflow="wrap" %}
```
curl "http://nft.chainup.net/scroll_mainnet/token/v1/isHolderOfContract?contract_address={CONTRACT_ADDRESS}&wallet={WALLET_ADDRESS}"
```
{% endcode %}
{% endtab %}

{% tab title="HoleSky" %}
{% code overflow="wrap" %}
```
curl "http://nft.chainup.net/eth_holesky/token/v1/isHolderOfContract?contract_address={CONTRACT_ADDRESS}&wallet={WALLET_ADDRESS}"
```
{% endcode %}
{% endtab %}
{% endtabs %}









