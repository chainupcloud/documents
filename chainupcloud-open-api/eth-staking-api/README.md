# ETH Staking API

This API allows you to interact with the staking process for the Ethereum blockchain. Here's a breakdown of the key functionalities:

The following are the steps for ETH staking/unstaking:

<figure><img src="../../.gitbook/assets/image (88).png" alt=""><figcaption><p>Creates new validator keys and returns a staking transaction to deposit ETH to those validators. A maximum of 100 validators can be created per request.</p></figcaption></figure>

### **Here are the five steps of the staking process:**

**1. Create Validators:**

* Use the Staking API to create special accounts called validators, up to 100 at once.
* The API provides an unsigned transaction that will deposit ETH to these validators.

**2. Sign Transaction:**

* Use your private key (like a secret password) to approve the unsigned transaction received from the API. **Never share this key with anyone!**
* Code examples for signing can be found on GitHub: \[ [https://github.com/chainupcloud/staking-demo-go/blob/main/examples/signed\_tx\_deposit\_test.go](https://github.com/chainupcloud/staking-demo-go/blob/main/examples/signed\_tx\_deposit\_test.go)  ] (see the example TestSignAndBroadcastTx only, do not execute code from unknown sources).

**3. Broadcast Transaction:**

* Two options for broadcasting the signed transaction:
  1. **Manual Broadcast:** Use the provided code for reference, but proceed only if you have technical expertise.
  2. **API Broadcast:** Simplify the process by using the Staking API endpoint `POST /api/v1/validator/broadcast`.

**4. Query Rewards:**

* Track your earnings using the Staking Rewards API.
* Get more information about specific validators using the Staking API endpoint `POST /api/v1/validator/details`.

**5. Exit (Optional):**

* To stop staking with a validator and withdraw your ETH, use the Staking API endpoint `POST /api/v1/validator/exit`.
* Expect a waiting period for funds to become available.

