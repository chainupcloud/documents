---
description: Delegate to any of our validators and staking networks that we support
---

# ⛲ How to generate Deposit Data?

A short guide on generating Deposit Data

### **Prerequisites**

**a.** A compatible wallet (currently only supports [**Metamask**](https://metamask.io/)) that holds more than 32 Eth

**b.** Generate `deposit_data-timestamp.json` which can be done through the [**deposit-cli tool**](https://github.com/ethereum/staking-deposit-cli/releases/).&#x20;

{% hint style="info" %}
Specifically, what we actually need is the `withdrawal_credentials` within the `deposit_data-timestamp.json`
{% endhint %}

### 1. Generating `deposit_data`/`withdrawal_credentials`

**Step 1:** Install the deposit-cli tool app [**here**](https://github.com/ethereum/staking-deposit-cli/releases/), ensuring you've selected the right one for your operating system.

{% hint style="warning" %}
Please make sure that you are downloading from the Ethereum Foundation's official GitHub account - [https://github.com/ethereum/staking-deposit-cli/releases/](https://github.com/ethereum/staking-deposit-cli/releases/)
{% endhint %}

<figure><img src="../../.gitbook/assets/deposit.png" alt=""><figcaption><p>Select the corresponding executable for your operating system</p></figcaption></figure>

**Step 2:** Once the download is complete, uncompress the downloaded file.

**Step 3:** Open your command line/terminal.

<figure><img src="../../.gitbook/assets/terminal.PNG" alt=""><figcaption><p>Open a terminal</p></figcaption></figure>

**Step 4:** navigate (`cd`) to the directory containing the executable **`deposit`** file.&#x20;

<figure><img src="../../.gitbook/assets/cd (2).PNG" alt=""><figcaption><p><code>cd</code> to the directory containing the executable</p></figcaption></figure>

**Step 5:** Generate a new BLS keystore using the deposit-cli new-keystore command. Run the executable with the following command `deposit.exe new-mnemonic --num_validators 1 --chain mainnet` for Windows and `./deposit new-mnemonic --num_validators 1 --chain mainnet` for Linux or MacOS.

Run the executable with the following command

{% tabs %}
{% tab title=" Linux or MacOS" %}
`./deposit new-mnemonic --num_validators 1 --chain mainnet for`
{% endtab %}

{% tab title="Windows " %}
&#x20;`deposit.exe new-mnemonic --num_validators 1 --chain mainnet`
{% endtab %}
{% endtabs %}

<figure><img src="../../.gitbook/assets/gg.PNG" alt=""><figcaption><p>Generate keys &#x26; <code>deposit_data</code></p></figcaption></figure>

**Step 6:** Note down the mnemonic phrase.\


{% hint style="info" %}
The mnemonic phrase is a 16/24-word phrase that is used to generate your validator keys. Keep it safe, write it down on paper or use a password manager, and store it where only you can access it.
{% endhint %}

<figure><img src="../../.gitbook/assets/depo.png" alt=""><figcaption></figcaption></figure>

After running through all the prompts and confirmations, the `deposit-cli` tool will generate two files for each validator:

* A deposit\_data-xxx.json file
* A keystore-m\_12381\_3600\_0\_0\_n\_xxx.json file

Keep these files safe. You will need them to manage your validator.

{% hint style="info" %}
You can find alternative key generating tools [here](https://ethereum.org/en/staking/solo/#key-generators) recommended by the Ethereum foundation.
{% endhint %}

