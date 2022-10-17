# Running Validator Node

A short guide to set up an Ethereum validator with [**ChainUp Cloud**](https://www.chainupcloud.com/) as your validator as a service provider. If you simply just want to stake Eth, it is recommended to check out the [**Ethereum Staking Guide**](../../introduction/for-investors/delegate-your-token.md) **** instead.

### **Prerequisites**

**a.** A compatible wallet (currently only supports [**Metamask**](https://metamask.io/)) that holds more than 32 Eth

**b.** Generate Validator Keys (`keystore_timestamp.json`), which can be done through the Ethereum launchpad ([**Mainnet**](https://launchpad.ethereum.org/en/overview), [**Goerli**](https://goerli.launchpad.ethereum.org/en/)) and the [**deposit-cli tool**](https://github.com/ethereum/staking-deposit-cli/releases/).&#x20;

**c.** Deposit 32 Eth (with your `deposit_data-timestamp.json`) either through the [**Abyss Eth2 Depositer**](https://abyss.finance/eth2depositor) (which currently supports only [**Mainnet**](https://etherscan.io/address/0xFA5f9EAa65FFb2A75de092eB7f3fc84FC86B5b18) and [**Goerli**](https://goerli.etherscan.io/address/0x2cB1A746A8652dfbb0FC11BdA71Bd991EB2Fd52e)) or Ethereum launchpad ([**Mainnet**](https://launchpad.ethereum.org/en/upload-deposit-data), [**Goerli**](https://goerli.launchpad.ethereum.org/en/upload-deposit-data)).&#x20;

### Eth2 Launchpad Demo Walkthrough

The following **video walkthrough** covers prerequisites **b** and **c**.&#x20;

{% embed url="https://www.youtube.com/watch?ab_channel=ConsenSysMedia&v=4jpzo9qOaP8" %}

### 1. Creating an Account

**Step 1:** Users are able to sign up on [**ChainUp Cloud**](https://app.chainupcloud.com/register).

![Sign Up](../../.gitbook/assets/chainupcloudregister.PNG)

**Step 2:** Login to [**ChainUp Cloud**](https://app.chainupcloud.com/login) with your newly created account.

![Login](../../.gitbook/assets/chainupcloudlogin.PNG)

### 2. Upload Validator Keys

**Step 1:** Click on **Ethereum 2** (sidebar). Make sure, you are in the **Ethereum2** subpage, and click on the **Host Button**.

<figure><img src="../../.gitbook/assets/2 (1).png" alt=""><figcaption><p>Eth2 Validator Dashboard</p></figcaption></figure>

{% hint style="info" %}
We assume users have already completed all the prerequisites prior to reaching this step
{% endhint %}

**Step 2:** Choose the network you are going to use and connect your [**Metamask**](https://metamask.io/) wallet.

<figure><img src="../../.gitbook/assets/15.PNG" alt=""><figcaption><p>Make Deposit - Hosting your own nodes</p></figcaption></figure>

{% hint style="info" %}
[**ChainUp Cloud**](https://www.chainupcloud.com/) is still providing support for the Ropsten Testnet. You can manually add the Ropsten network to your wallet with our [**Blockchain API**](../../introduction/products/blockchain-api.md).
{% endhint %}

**Step 3:** If you have deposited 32 Eth through the official staking launchpad or [**Abyss Eth2 Depositer**](https://abyss.finance/eth2depositor) (prerequisites **b** and **c**), the wallet details should be reflected on the dashboard.

<figure><img src="../../.gitbook/assets/16.png" alt=""><figcaption><p>Make Deposit - Check Your Wallet Details</p></figcaption></figure>

**Step 4:** Create validator by checking **Yes** for the following two options.&#x20;

<figure><img src="../../.gitbook/assets/14.PNG" alt=""><figcaption><p>Create validator</p></figcaption></figure>

**Step 5:**  Import the keys (`keystore_timestamp.json`) and password - this has been generated from the `deposit-cli` tool by following the **** [**video above**](https://www.youtube.com/watch?v=4jpzo9qOaP8\&ab\_channel=ConsenSysMedia).&#x20;

<figure><img src="../../.gitbook/assets/5.png" alt=""><figcaption><p>Import Keys - upload deposit_data.json </p></figcaption></figure>

**Step 6:** Done and set! You can now click through the confirmation steps and validator should be active soon.&#x20;

<figure><img src="../../.gitbook/assets/12.png" alt=""><figcaption><p>Dashboard showing validator status. </p></figcaption></figure>

{% hint style="info" %}
After the initial 32 Eth deposit, you may check back after some time or so, as it may take [**more than 12 hours**](https://kb.beaconcha.in/ethereum-2.0-depositing) for a transaction to reach the deposit contract on Beacon Chain.
{% endhint %}

[**Sign up now**](https://app.chainupcloud.com/register) to start running your own validators and discover the wonders of ChainUp Cloud!
