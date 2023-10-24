---
description: >-
  In this tutorial, we'll guide you through the process of generating your
  Validator Keys. These keys are not just random numbers—they are the digital
  keys to your assets and transactions, ensuring tha
---

# How to create Validator Keys?

### **Prerequisites**

**a.** A compatible wallet (currently only supports [**Metamask**](https://metamask.io/)) that holds more than 32 Eth

**b.** Generate `deposit_data-timestamp.json` which can be done through the [**deposit-cli tool**](https://github.com/ethereum/staking-deposit-cli/releases/).&#x20;

{% hint style="info" %}
Specifically, what we actually need is the `withdrawal_credentials` within the `deposit_data-timestamp.json`
{% endhint %}

### 1. Generating `deposit_data`/`withdrawal_credentials`

**Step 1:** Download the deposit CLI app [**here**](https://github.com/ethereum/staking-deposit-cli/releases/), ensuring you've selected the right one for your operating system.

{% hint style="warning" %}
Please make sure that you are downloading from the Ethereum Foundation's official GitHub account - [https://github.com/ethereum/staking-deposit-cli/releases/](https://github.com/ethereum/staking-deposit-cli/releases/)
{% endhint %}

<figure><img src="../../.gitbook/assets/deposit.png" alt=""><figcaption><p>Select the corresponding executable for your operating system</p></figcaption></figure>

**Step 2:** Once the download is complete, uncompress the downloaded file.

**Step 3:** Open your command line/terminal.

<figure><img src="../../.gitbook/assets/terminal.PNG" alt=""><figcaption><p>Open a terminal</p></figcaption></figure>

**Step 4:** navigate (`cd`) to the directory containing the executable **`deposit`** file.&#x20;

<figure><img src="../../.gitbook/assets/cd (2).PNG" alt=""><figcaption><p><code>cd</code> to the directory containing the executable</p></figcaption></figure>

**Step 5:** Run the executable with the following command `deposit.exe new-mnemonic --num_validators 1 --chain mainnet` for Windows and `./deposit new-mnemonic --num_validators 1 --chain mainnet` for Linux or MacOS.

<figure><img src="../../.gitbook/assets/gg.PNG" alt=""><figcaption><p>Generate keys &#x26; <code>deposit_data</code></p></figcaption></figure>

**Step 6:** <mark style="color:red;">Please note down the mnemonic phrase</mark> and locate the `deposit_data` file

<figure><img src="../../.gitbook/assets/depo.png" alt=""><figcaption><p><code>deposit_data</code> file will be uploaded to ChainUp Cloud later</p></figcaption></figure>

{% hint style="info" %}
You can find alternative key generating tools [here](https://ethereum.org/en/staking/solo/#key-generators) recommended by the Ethereum foundation.
{% endhint %}
