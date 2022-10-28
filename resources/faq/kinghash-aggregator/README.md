# 🍧 KingHash Aggregator

## :gear:General

### What is KingHash Aggregator?

KingHash Aggregator is a smart contract that leverages cutting-edge, innovative algorithms that can help users to discover the best staking strategies.

### How does KingHash Aggregator works?

KingHash have a set of strategies which each optimize different parameters. KingHash's backend will run various financial simulations, and provide various strategies for the user to select. In the future, the user is also feel free to select and create their own strategy.&#x20;

Subsequently, user can select and sign the transaction which will interact with KingHash Aggregator smart contract and distribute Eth to the various protocols.

### Why should I use KingHash Aggregator?

Lower risks, higher rewards and better decentralization. Users can spread their risks by staking their Eth across multiple protocols, a single [Blackswan event](https://en.wikipedia.org/wiki/Black\_swan\_theory) would not affect all your investments. This can also result in higher yield thanks to the [modern portfolio theory](https://www.investopedia.com/terms/m/modernportfoliotheory.asp). And most importantly, you will help in the decentralization of Ethereum by spreading your Eth across various protocols!

### How does the Validator NFT works?

KingHash Aggregator uses the Validator NFT Contract as one of its many strategies. The Validator NFT currently can be minted through the KingHash Aggregator Contract.&#x20;

Each Validator NFT corresponds to an actual physical node somewhere in the world. It can traded on NFT marketplaces such as Opensea or on our platform. As it is an actual Validator node, it produces rewards overtime. KingHash's Validator NFT by default utilizes MEV-boost technology to maximize Ethereum rewards. Along with our other proprietary software and inventions, we are able to increase validator rewards **significantly** and reward holders **handsomely**.

{% hint style="info" %}
We welcome any Blockchain Infrastructure Company/Institutions & reputable individuals who wishes to publish their own Validator NFT and integrate with us. Our code is Open Source and [available on Github](https://github.com/ChainUp-Cloud).
{% endhint %}

### How are rewards calculated for the Validator NFT?

Assuming $$N$$ is the total number of Validator NFTs, $$gas\_height_i$$ is the block height which the reward of the NFT is last claimed previously, and $$\alpha$$ is the commission required to keep the node operating. Then the reward of the Validator NFT $$i$$ is given by the following formula:&#x20;

$$Reward_i = (1 - \alpha)\frac{total\_reward \times (current\_height - gas\_height_i)}{N \times current\_height - \sum_{n=1}^{N} gas\_height_n}$$

This ensures that each NFT holder get their fair share of reward proportional to the duration of staking.

## :rocket:Onboarding

### How to create a ChainUp Cloud account?

You do not need a ChainUp Cloud account to use KingHash Aggregator, it is permissionless in nature.&#x20;

Nonetheless, you can use any email account to sign up for ChainUp Cloud easily. With ChainUp Cloud account, you can get access to a variety of services such as Blockchain API, Validator Nodes and more. To do this, go to [https://cloud.chainup.com/app/register](https://cloud.chainup.com/app/register)

## 💰Pricing <a href="#pricing" id="pricing"></a>

### Is it free to use KingHash Aggregator? <a href="#is-it-free-to-use-chainup-clouds-services" id="is-it-free-to-use-chainup-clouds-services"></a>

Yes. It is a smart contract that anyone can interact with. You can even integrate KingHash Aggregator into your applications by using KingHash's [API](../../../introduction/for-developers/use-kinghash-aggregator-api.md).

### Is the Validator NFT free?

Yes. The Validator NFT is completely free. The cost to operate the node is subtracted though the commission fees.
