---
description: Returns validators for your organization (via API key).
---

# Get Validators

**HTTP Request**

```HTTP
POST /api/v1/validator/details
```

**Path Params**No param\
**Request Params**

| **Parameter name**  | **Data type** | **Whether it must be passed.** | **Description**                                                     |
| ------------------- | ------------- | ------------------------------ | ------------------------------------------------------------------- |
| pubkeys             | array         | false                          | Verifier list                                                       |
| withdrawal\_address | string        | false                          | Withdrawal address                                                  |
| page                | int           | false                          | Page number (default is 1)                                          |
| limit               | int           | false                          | Number of entries per page (default is 10, maximum support is 1000) |

\
**Response**

| **Parameter name**        | **Data type** | **Description**                                                    |
| ------------------------- | ------------- | ------------------------------------------------------------------ |
| network                   | string        | network                                                            |
| pubkey                    | string        | pubkey                                                             |
| withdrawal\_address       | string        | Consensus layer withdrawal address                                 |
| withdrawal\_credentials   | string        | Consensus layer withdrawal voucher                                 |
| fee\_recipient\_address   | string        | Execution layer reward receiving address                           |
| deposit\_from\_address    | string        | Deposit from address                                               |
| status                    | string        | Validator status: https://hackmd.io/@protolambda/validator\_status |
| slashed                   | boolean       | Was slashed                                                        |
| activation\_epoch         | string        | <p><br></p>                                                        |
| exit\_epoch               | string        | <p><br></p>                                                        |
| withdrawable\_epoch       | string        | <p><br></p>                                                        |
| estimated\_active\_at     | string        | Estimated activation time                                          |
| estimated\_exit\_at       | string        | Estimated exit time                                                |
| estimated\_withdrawal\_at | string        | Estimated withdrawal time                                          |
| is\_need\_exit            | boolean       | Whether to initiate an exit                                        |
| is\_post\_exit            | boolean       | Whether the exit request is broadcast to the chain                 |

\
**Example**

```JSON
{
    "code": "200",
    "msg": "Success",
    "pagination": {
       "page": 1,
       "limit": 10,
       "total": 2
    },
    "data": [
        {
            "network": "holesky",
            "pubkey": "0xd1ef8d468ef53d82368d2026e321ab2c6d44f44c33b7b9f22369bf6dcf37fb0208f82dd6b485325ce1bbf5aec7ad45bb",
            "withdrawal_address": "0xE40F80618324C814cD444434670a44ba4583aE38",
            "withdrawal_credentials": "0x010000000000000000000000fc438e6cc4b230eb5bfaae1337c3f5da2b9140f1",
            "fee_recipient_address": "0x781462762B706AA7c1DA71FBA1a545724928b81f",
            "deposit_from_address": "0xE40F80618324C814cD444434670a44ba4583aE38",
            "status": "active_ongoing",
            "slashed": false,
            "activation_epoch": "0",
            "exit_epoch": "18446744073709551615",
            "withdrawable_epoch": "18446744073709551615",
            "status_estimates": {
                "estimated_active_at": "2023-07-01T00:00:00.000Z",
                "estimated_exit_at": "2023-07-01T00:00:00.000Z",
                "estimated_withdrawal_at": "2023-07-01T00:00:00.000Z"
            },
            "is_need_exit": false,
            "is_post_exit": false
        }
    ]
}
```
