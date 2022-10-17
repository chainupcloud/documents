# 👥 Running your own validators

A short guide to start setting up a Ethereum validator with [**ChainUp Cloud**](https://www.chainupcloud.com/) as your node as a service provider.

### **Prerequisites**

**a.** A compatible wallet (currently only supports [**Metamask**](https://metamask.io/)) that holds more than 32 Eth

**b.** Generate Deposit data (`deposit_data-[timestamp].json`) which is through the Ethereum launchpad ([**Mainnet**](https://launchpad.ethereum.org/en/overview), [**Goerli**](https://goerli.launchpad.ethereum.org/en/)) and the [**deposit-cli tool**](https://github.com/ethereum/staking-deposit-cli/releases/).&#x20;

**c.** Deposit 32 Eth either through Ethereum launchpad ([**Mainnet**](https://launchpad.ethereum.org/en/overview), [**Goerli**](https://goerli.launchpad.ethereum.org/en/)) or through the [**Abyss Eth2 Depositer**](https://abyss.finance/eth2depositor) (which currently supports only [**Mainnet**](https://etherscan.io/address/0xFA5f9EAa65FFb2A75de092eB7f3fc84FC86B5b18) and [**Goerli**](https://goerli.etherscan.io/address/0x2cB1A746A8652dfbb0FC11BdA71Bd991EB2Fd52e)).&#x20;

### Eth2 Launchpad Demo Walkthrough

The following **video walkthrough** covers prerequisites **b** and **c**.&#x20;

{% embed url="https://www.youtube.com/watch?ab_channel=ConsenSysMedia&v=4jpzo9qOaP8" %}

### 1. Creating an Account

**Step 1:** Users are able to sign up on [**ChainUp Cloud**](https://app.chainupcloud.com/register).

![Sign Up](../../.gitbook/assets/chainupcloudregister.PNG)

**Step 2:** Login to [**ChainUp Cloud**](https://app.chainupcloud.com/login) with your newly created account.

![Login](../../.gitbook/assets/chainupcloudlogin.PNG)

### 2. Make Deposit

**Step 1:** Click on Ethereum 2 (sidebar). Make sure, you are in the _Ethereum2_ subpage, and click on the _Host Button_

<figure><img src="../../.gitbook/assets/2 (1).png" alt=""><figcaption><p>Eth2 Validator Dashboard</p></figcaption></figure>

**Step 3:** Choose the network you are going to use and connect your [**Metamask**](https://metamask.io/) wallet.&#x20;

<figure><img src="../../.gitbook/assets/15.PNG" alt=""><figcaption><p>Make Deposit - Hosting your own nodes</p></figcaption></figure>

**Step 4:** If you have deposited 32 Eth through the official staking launchpad or [**Abyss Eth2 Depositer**](https://abyss.finance/eth2depositor) (prerequisites **b** and **c**), the wallet details will be as shown. &#x20;

<figure><img src="../../.gitbook/assets/16.png" alt=""><figcaption><p>Make Deposit - Check Your Wallet Details</p></figcaption></figure>

**Step 5 :** Create Validator by checking Yes for the following two options.&#x20;

<figure><img src="../../.gitbook/assets/14.PNG" alt=""><figcaption><p>Create Validator</p></figcaption></figure>

**Step 6:**  Import the keys (`keystore-m_timestamp.json`) - this has been generated from the `deposit-cli` tool by following the **** [**video above**](https://www.youtube.com/watch?v=4jpzo9qOaP8\&ab\_channel=ConsenSysMedia).&#x20;

<figure><img src="../../.gitbook/assets/5.png" alt=""><figcaption><p>Import Keys - upload deposit_data.json </p></figcaption></figure>

Step 7 : Done and set! Your validator is now active.&#x20;

<figure><img src="../../.gitbook/assets/12.png" alt=""><figcaption><p>Dashboard showing validator status. </p></figcaption></figure>

**Please note:** after the initial 32 Eth deposit, you may check back after some time or so, as it may take more than 12 hours for a transaction to reach the deposit contract on Beacon Chain.
