# Ownership & Token Gating

<mark style="color:blue;">`GET`</mark> `/nft/{chain}/{token}/getContractsForOwner`     &#x20;

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



<mark style="color:blue;">`GET`</mark> `/nft/{chain}/{token}/getNFTsForOwner`             &#x20;

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



<mark style="color:blue;">`GET`</mark> `/nft/{chain}/{token}/getOwnersForContract`           &#x20;

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





<mark style="color:blue;">`GET`</mark> `/nft/{chain}/{token}/getOwnersForNFT`           &#x20;

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



<mark style="color:blue;">`GET`</mark> `/nft/{chain}/{token}/isHolderOfContract`&#x20;

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









