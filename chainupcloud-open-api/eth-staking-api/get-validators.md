---
description: This API endpoint allows you to retrieve information about your validators.
---

# Get Validators

### **HTTP Request**

Use a `POST` request to the endpoint.

```HTTP
POST /api/v1/validator/details
```

### **Path Params:** No param 

### **Request Params**

#### **Request:**

* Use a `POST` request to the `/api/v1/validator/details` endpoint.
* You can optionally provide:
  * **pubkeys (array):** List of specific validator keys to query (if empty, all your validators are included).
  * **withdrawal\_address:** Filter validators by their withdrawal address.
  * **Pagination details (page & limit):** Control the number of results displayed per page.

<table data-header-hidden><thead><tr><th width="205"></th><th></th><th></th><th></th></tr></thead><tbody><tr><td><strong>Parameter name</strong></td><td><strong>Data type</strong></td><td><strong>Whether it must be passed.</strong></td><td><strong>Description</strong></td></tr><tr><td>pubkeys</td><td>array</td><td>false</td><td>Verifier list</td></tr><tr><td>withdrawal_address</td><td>string</td><td>false</td><td>Withdrawal address</td></tr><tr><td>page</td><td>int</td><td>false</td><td>Page number (default is 1)</td></tr><tr><td>limit</td><td>int</td><td>false</td><td>Number of entries per page (default is 10, maximum support is 1000)</td></tr></tbody></table>

### **Response**

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
