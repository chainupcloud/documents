# Staking API



Overview

The following are the steps for ETH staking/unstaking:

<figure><img src="../../.gitbook/assets/image (88).png" alt=""><figcaption><p>Creates new validator keys and returns a staking transaction to deposit ETH to those validators. A maximum of 250 validators can be created per request.</p></figcaption></figure>



**Sign & Broadcast Tx**  Sign step, you need to **Create Validators** return value private key signature, the implementation example can be seen in `TestSignTx` : https://github.com/chainupcloud/staking-demo-go/blob/main/examples%2Fsigned\_tx\_deposit\_test.goBroadcast steps, need to broadcast signdeTx on the blockchain, this step:

* You can do it yourself, see the example `TestSignAndBroadcastTx` : https://github.com/chainupcloud/staking-demo-go/blob/main/examples%2Fsigned\_tx\_deposit\_test.go
* It can also be implemented by calling the API: POST /api/v1/validator/broadcast

\
**Query Validators & Rewards**  \
Use the Staking Rewards API to view validator rewards.View some information about yalidator via POST /api/v1/validator/details .\
**Exit Validators**&#x20;

Unstake ETH & Exit validators by POST /api/v1/validator/exit\


