---
description: Quick start guide for Web3 developers
---

# 🍧 Use KingHash Aggregator API

## Quick Description

KingHash Aggregator API allows developers to query and expose all data related to staking. Users can query all sort of staking strategies, trade their validator nodes and check their balances. Developers can also integrate KingHash Aggregator API into their applications. This means customers of all sizes, from small app developers to exchanges and custodians can safely implement staking-facing products for their users.

## Benefits

### Maximize yield when staking on Ethereum

KingHash Aggregator is the only protocol out there which maximizes staking yield on Ethereum by integrating with all other existing staking protocols. It is not possible to get any better yield out there.

### Easy to Integrate

KingHash Aggregator is extremely easy to integrate. Calling the API returns a prepared transaction which can be signed by any wallets! All developers need to do is call the API and prepare a frontend for users to interact with.

### Transparent staking experience

The staking transaction is done completely on-chain, users can see how much they stake and where their Ether went. They have full control of their assets at all times and ownership left leave their wallets.

## API

{% swagger src="https://chainupcloud.github.io/swagger/swagger.json" path="/quote/stake" method="post" %}
[https://chainupcloud.github.io/swagger/swagger.json](https://chainupcloud.github.io/swagger/swagger.json)
{% endswagger %}

{% swagger src="https://chainupcloud.github.io/swagger/swagger.json" path="/quote/unstake" method="post" %}
[https://chainupcloud.github.io/swagger/swagger.json](https://chainupcloud.github.io/swagger/swagger.json)
{% endswagger %}

{% swagger src="https://chainupcloud.github.io/swagger/swagger.json" path="/quote/routes" method="get" %}
[https://chainupcloud.github.io/swagger/swagger.json](https://chainupcloud.github.io/swagger/swagger.json)
{% endswagger %}

{% swagger src="https://chainupcloud.github.io/swagger/swagger.json" path="/address/balance" method="get" %}
[https://chainupcloud.github.io/swagger/swagger.json](https://chainupcloud.github.io/swagger/swagger.json)
{% endswagger %}

{% swagger src="https://chainupcloud.github.io/swagger/swagger.json" path="/address/validator" method="get" %}
[https://chainupcloud.github.io/swagger/swagger.json](https://chainupcloud.github.io/swagger/swagger.json)
{% endswagger %}

{% swagger src="https://chainupcloud.github.io/swagger/swagger.json" path="/nft/list" method="post" %}
[https://chainupcloud.github.io/swagger/swagger.json](https://chainupcloud.github.io/swagger/swagger.json)
{% endswagger %}

{% swagger src="https://chainupcloud.github.io/swagger/swagger.json" path="/nft/cancel_listing" method="post" %}
[https://chainupcloud.github.io/swagger/swagger.json](https://chainupcloud.github.io/swagger/swagger.json)
{% endswagger %}

{% swagger src="https://chainupcloud.github.io/swagger/swagger.json" path="/nft/listings" method="get" %}
[https://chainupcloud.github.io/swagger/swagger.json](https://chainupcloud.github.io/swagger/swagger.json)
{% endswagger %}

{% swagger src="https://chainupcloud.github.io/swagger/swagger.json" path="/nft/buy" method="post" %}
[https://chainupcloud.github.io/swagger/swagger.json](https://chainupcloud.github.io/swagger/swagger.json)
{% endswagger %}

{% embed url="https://chainupcloud.github.io/swagger/" %}
Swagger docs
{% endembed %}

{% hint style="info" %}
`source` - Can be used by developers to keep track of requests from different applications by providing different strings
{% endhint %}
