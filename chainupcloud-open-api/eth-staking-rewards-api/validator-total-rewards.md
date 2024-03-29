---
description: >-
  This API endpoint provides a comprehensive overview of your validator rewards
  and overall staking status.
---

# Validator Total Rewards

### **HTTP Request**

```HTTP
Get /api/v1/validator/total-rewards
```

**Path Params :** No param

### **Request Params**

| **Parameter name** | **Data type** | **Whether it must be passed.** | **Description**                                                       |
| ------------------ | ------------- | ------------------------------ | --------------------------------------------------------------------- |
| page               | int           | false                          | Page number (default is 1)                                            |
| limit              | int           | false                          | Number of entries per page (default is 10 , maximum support is 1000 ) |

### **Response**

<table data-header-hidden><thead><tr><th></th><th width="193"></th><th></th></tr></thead><tbody><tr><td><strong>Parameter name</strong></td><td><strong>Data type</strong></td><td><strong>Description</strong></td></tr><tr><td>el_total_reward<br></td><td>string</td><td>Total revenue of the execution layer (unit: eth) (real revenue on the chain, if there is settlement, it needs to be calculated separately)</td></tr><tr><td>cl_total_reward</td><td>string</td><td>Total revenue of consensus layer (unit: eth)</td></tr><tr><td>total_reward</td><td>string</td><td>Total revenue of execution layer + consensus layer (unit: eth)</td></tr><tr><td>cl_balance</td><td>string</td><td>Consensus layer balance (unit: eth)</td></tr><tr><td>effective_balance</td><td>string</td><td>Effective balance of consensus layer (unit: eth)</td></tr><tr><td>status</td><td>string</td><td>Validator status</td></tr><tr><td>validators_active_count</td><td>int</td><td>Number of active validators</td></tr><tr><td>validators_total_count</td><td>int</td><td>Total number of validators</td></tr><tr><td>validators_total_rewards</td><td>string</td><td>Cumulative total rewards for validators</td></tr><tr><td>validators_total_cl_balance</td><td>string</td><td>Validator consensus layer total balance</td></tr></tbody></table>

### **Example:**

```JSON
{
    "code": "200",
    "msg": "Success",
    "pagination": {
        "page": 1,
        "limit": 10,
        "total": 2
    },
    "data": {
        "validator_details": [
            {
                "validator_index": 1,
                "pubkey":"0x8000025593183bad1730e78b87b6bce428492e3bf9142d2609032daf674596f955d6403481c7d84809905a262c0136e2",
                "el_total_reward": "0.039144409",
                "cl_total_reward": "0.0446064811764954",
                "total_reward": "0.0837508901764954",
                "cl_balance": "32.0837508901764954",
                "effective_balance": "32",
                "status": "active"
            },
            {
                "validator_index": 2,
                "pubkey":"0x8000091c2ae64ee414a54c1cc1fc67dec663408bc636cb86756e0200e41a75c8f86603f104f02c856983d2783116be13",
                "el_total_reward": "0.039144409",
                "cl_total_reward": "0.0446064811764954",
                "total_reward": "0.0837508901764954",
                "cl_balance": "32.0837508901764954",
                "effective_balance": "32",
                "status": "active"
            }
        ],
        "validators_active_count": 2,
        "validators_total_count": 2,
        "validators_total_rewards": "0.3246064811764954",
        "validators_total_cl_balance": "64.3246064811764954"
    }
}
```
