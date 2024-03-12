# Create Validators

### Create Validators

Creates new validator keys and returns a staking transaction to deposit ETH to those validators. A maximum of 100 validators can be created per request.\


> Note: This API needs to generate validator keys, which is a time-consuming operation with a peak value of 100 keys. This interface takes about 20 seconds.

{% hint style="info" %}
Note: This API needs to generate validator keys, which is a time-consuming operation. The peak number is 100 keys. This API takes about 20 seconds.
{% endhint %}

**HTTP Request**

```HTTP
POST /api/v1/validator/create
```

**Path Params :** No param\
**Request Params**

| **Parameter name**      | **Data type** | **Whether it must be passed.** | **Description**                                                        |
| ----------------------- | ------------- | ------------------------------ | ---------------------------------------------------------------------- |
| validator\_count        | int           | true                           | Number of validators (maximum: 100)                                    |
| withdrawal\_address     | string        | true                           | Withdrawal address                                                     |
| deposit\_from\_address  | string        | false                          | Deposit address, default value is: withdrawal\_address                 |
| fee\_recipient\_address | string        | false                          | Execution layer revenue address, default value is: withdrawal\_address |

\
**Response**\
**Example**

```JSON
{
    "code": "200",
    "msg": "Success",
    "data": {
        "validators": [
            {
                "network": "holesky",
                "pubkey": "0xd1ef8d468ef53d82368d2026e321ab2c6d44f44c33b7b9f22369bf6dcf37fb0208f82dd6b485325ce1bbf5aec7ad45bb",
                "amount_wei": "32000000000000000000",
                "withdrawal_address": "0xE40F80618324C814cD444434670a44ba4583aE38",
                "deposit_from_address": "0xE40F80618324C814cD444434670a44ba4583aE38",
                "fee_recipient_address": "0xE40F80618324C814cD444434670a44ba4583aE38",
                "deposit_data": {
                    "amount": 32000000000,
                    "signature": "0xaab7e3b41689fced6c3437a6bc5caf471ed319b94ad2642c47c5f641d5e3a046432171d47d48cd7a3e8a323939d4976c1315ad4dae134c421214673ddff9105ef1bb7f79c1babc6cd9c31428d5e44472164e9c9fccfd10fb9768c0855b194f49",
                    "deposit_data_root": "0xb2f5083221d6b61f2237af155c07c746f6a75c7d24dfe418106efdf87e9b9422",
                    "deposit_message_root": "0x026cbefa013e03a3d81592b7a5f6205773c12a6f7674529e497e9a4eb2df2d44",
                    "fork_version": "0x00000000"
                }
            }
        ],
        "staking_transaction": {
            "from": "0xE40F80618324C814cD444434670a44ba4583aE38",
            "to": "0x94a2da805867c962148d3832d9afc512034a62c5",
            "amount_wei": "32000000000000000000",
            "contract_call_data": "0x4f498c730000000000000000000000000000000000000000000000000000000000000080000000000000000000000000000000000000000000000000000000000000012000000000000000000000000000000000000000000000000000000000000001a000000000000000000000000000000000000000000000000000000000000002600000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000308dc141dc3a91a5b09dca7e9eb1c0f1f6cac2cad68ffc478956b741b1d9318285f31434fbcd7b3ae31697d772ba9d767600000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000200000000000000000000000000000000000000000000000000000000000000020010000000000000000000000f60e717ce428e7d1d61e147aa34f1595caa56669000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000200000000000000000000000000000000000000000000000000000000000000060b29edc85070d565b7a5e4f1d86443979231b4152be44b03cfe94c5b96101f51e70eaa488030dd5a8ae10412ae0c64d9716fb7248cc9e94adb8b62e9025de645a46f05b767d9100ef5587c3bc0ebb78f12ff3b821417e97e36dcd8ff2376ca9c400000000000000000000000000000000000000000000000000000000000000010cf3e3a73ec22d7278d7b54ba88ae24013e5370bc263e4b3a26fef09b1b1946d",
        }
    }
}
```

