# Validator Total Rewards

**Query user's validator history cumulative rewards**

\
**HTTP Request**

```HTTP
Get /api/v1/validator/total-rewards
```

**Path Params**No param\
**Request Params**

| **Parameter name** | **Data type** | **Whether it must be passed.** | **Description**                                                       |
| ------------------ | ------------- | ------------------------------ | --------------------------------------------------------------------- |
| page               | int           | false                          | Page number (default is 1)                                            |
| limit              | int           | false                          | Number of entries per page (default is 10 , maximum support is 1000 ) |

\
**Response**

| **Parameter name**             | **Data type** | **Description**                                                                                                                            |
| ------------------------------ | ------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| <p>el_total_reward<br></p>     | string        | Total revenue of the execution layer (unit: eth) (real revenue on the chain, if there is settlement, it needs to be calculated separately) |
| cl\_total\_reward              | string        | Total revenue of consensus layer (unit: eth)                                                                                               |
| total\_reward                  | string        | Total revenue of execution layer + consensus layer (unit: eth)                                                                             |
| cl\_balance                    | string        | Consensus layer balance (unit: eth)                                                                                                        |
| effective\_balance             | string        | Effective balance of consensus layer (unit: eth)                                                                                           |
| status                         | string        | Validator status                                                                                                                           |
| validators\_active\_count      | int           | Number of active validators                                                                                                                |
| validators\_total\_count       | int           | Total number of validators                                                                                                                 |
| validators\_total\_rewards     | string        | Cumulative total rewards for validators                                                                                                    |
| validators\_total\_cl\_balance | string        | Validator consensus layer total balance                                                                                                    |

**Example:**

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
