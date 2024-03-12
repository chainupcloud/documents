# Cloud Validator Settles EL Rewards

**Query user cloud platform online settlement validator settlement execution layer reward listHTTP Request**

```HTTP
Get /api/v1/cloud/validator/el/settle/rewards
```

**Path Params**No param\
**Request Params**

| **Parameter name** | **Data type** | **Whether it must be passed.** | **Description**                                                                                                                       |
| ------------------ | ------------- | ------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------- |
| start\_date        | string        | false                          | Start date (YYYY-MM-DD) (UTC + 8)                                                                                                     |
| end\_date          | string        | false                          | End date (YYYY-MM-DD) (UTC + 8)                                                                                                       |
| validator\_indexes | array         | false                          | Validator index list (if empty, query all validators of the user by default; if not empty, query the data of the specified validator) |
| page               | int           | false                          | Page number (default is 1)                                                                                                            |
| limit              | int           | false                          | Number of entries per page (default is 10, maximum support is 1000)                                                                   |

**Note: Request date limit is up to one month**

1. end\_date cannot be greater than the current date.
2. start\_date cannot be greater than the current date.
3. This interface only supports querying mainnet reward data
4. This interface only supports queries. The current time node index exists on the cloud platform and there is index data for block reward data

**Example:**start\_date="2023-07-01"end\_date="2023-07-03"**Response**

| **Parameter name** | **Data type** | **Description**       |
| ------------------ | ------------- | --------------------- |
| pubkey             | string        | Public key            |
| validator\_index   | int           | Validator index       |
| fee\_address       | string        | Fee addres            |
| el\_reward         | string        | Block sales revenue   |
| fee\_rate          | string        | Service charge ratio  |
| user\_reward       | string        | User benefits         |
| service\_fee       | string        | Service charge        |
| reward\_time       | string        | Block production time |
| block\_number      | int           | Block height          |

**Example:**

```JSON
{
    "code": "200",
    "msg": "Success",
    "data": {
        "rewards": [
            {
                "id": 1740,
                "pubkey": "0x93943bd530b79623af943a2af636f06c327203d82784fafda621439438c418bd8d26c82061bbc956fc7f0f8ddb138173",
                "validator_index": 510848,
                "fee_address": "0xade4A1e54a0efA7c0557e8fdecC714F716eD0Be6",
                "el_reward": "0.0197237331857824",
                "fee_rate": "0.3",
                "user_reward": "0.01380661323004768",
                "service_fee": "0.00591711995573472",
                "reward_time": "2023-08-07 17:45:47",
                "block_number": 17864629
            },{
                "id": 1739,
                "pubkey": "0x93943bd530b79623af943a2af636f06c327203d82784fafda621439438c418bd8d26c82061bbc956fc7f0f8ddb138173",
                "validator_index": 510848,
                "fee_address": "0xade4A1e54a0efA7c0557e8fdecC714F716eD0Be6",
                "el_reward": "0.0534498763287165",
                "fee_rate": "0.3",
                "user_reward": "0.03741491343010155",
                "service_fee": "0.01603496289861495",
                "reward_time": "2023-08-04 21:15:11",
                "block_number": 17844231
            }
        ],
        "sum_reward": "0.496150059064933",
        "sum_service_fee": "0.212635739599257"
    },
    "pagination": {
        "page": 1,
        "limit": 2,
        "total": 11
    }
}
```
