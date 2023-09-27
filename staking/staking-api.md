# Staking API



Base URL & Auth

http://staking.chainup.net/${protocol}/mainnet/${token}\
**Support agreement**

| Agreement | Network |
| --------- | ------- |
| ethereum  | mainnet |

\
**Path Params**

| **Parameter name** | **Data type** | **Whether it must be passed.** | **Description**                                                                |
| ------------------ | ------------- | ------------------------------ | ------------------------------------------------------------------------------ |
| protocol           | string        | true                           | Protocol (ethereum)                                                            |
| token              | string        | true                           | The user is bound to the token of Staking and authenticated through the token. |

\
**Create token**

1. ChainUp creates a token and sends it to the customer via email.
2. User side generates Token.

\


### ETH Staking API

> Only count validators of ChainUpCloud platform.

#### Validator Total Rewards

**Query user's validator history cumulative reward**\
**HTTP Request**

```HTTP
Get /api/v1/validator/total-rewards
```

**Path Params**No param\
**Request Params**

| **Parameter name** | **Data type** | **Whether it must be passed.** | **Description**                                                  |
| ------------------ | ------------- | ------------------------------ | ---------------------------------------------------------------- |
| page               | int           | false                          | Page number (default is 1)                                       |
| limit              | int           | false                          | Number of articles per page (default 10 , maximum support 1000 ) |

\
**Response**

| **Parameter name**             | **Data type** | **Description**                                                                                                                                    |
| ------------------------------ | ------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| el\_total\_reward              | string        | Total revenue of the execution layer (unit: eth) (real revenue on the chain, if there is a commission ratio, it needs to be calculated separately) |
| cl\_total\_reward              | string        | Total revenue of consensus layer (unit: eth)                                                                                                       |
| total\_reward                  | string        | Total revenue of execution layer + consensus layer (unit: eth)                                                                                     |
| cl\_balance                    | string        | Consensus layer balance (unit: eth)                                                                                                                |
| effective\_balance             | string        | Effective balance of consensus layer (unit: eth)                                                                                                   |
| status                         | string        | Validator status                                                                                                                                   |
| <p>current_balance<br></p>     | string        | el\_total\_reward + cl\_total\_reward + effective\_balance (in eth)                                                                                |
| validators\_active\_count      | int           | Number of active validators                                                                                                                        |
| validators\_total\_count       | int           | Total number of validators                                                                                                                         |
| validators\_total\_rewards     | string        | Validator Cumulative Total Rewards                                                                                                                 |
| validators\_total\_cl\_balance | string        | Validator consensus layer total balance                                                                                                            |

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
                "status": "active",
                "current_balance": "32.1246064811764954"
            },
            {
                "validator_index": 2,
                "pubkey":"0x8000091c2ae64ee414a54c1cc1fc67dec663408bc636cb86756e0200e41a75c8f86603f104f02c856983d2783116be13",
                "el_total_reward": "0.039144409",
                "cl_total_reward": "0.0446064811764954",
                "total_reward": "0.0837508901764954",
                "cl_balance": "32.0837508901764954",
                "effective_balance": "32",
                "status": "active",
                "current_balance": "32.1246064811764954"
            }
        ],
        "validators_active_count": 2,
        "validators_total_count": 2,
        "validators_total_rewards": "0.3246064811764954",
        "validators_total_cl_balance": "64.3246064811764954"
    }
}
```

\


#### Validator Daily Rewards

**Query the daily reward within the specified date of the user verifierHTTP Request**

```HTTP
Get /api/v1/validator/daliy-rewards
```

**Path Params**No param\
**Request Params**

| **Parameter name** | **Data type** | **Whether it must be passed.** | **Description**                                                 |
| ------------------ | ------------- | ------------------------------ | --------------------------------------------------------------- |
| start\_date        | string        | false                          | Start date (YYYY-MM-DD) (UTC + 8)                               |
| end\_date          | string        | false                          | End date (YYYY-MM-DD) (UTC + 8)                                 |
| page               | int           | false                          | Page number (default is 1)                                      |
| limit              | int           | false                          | Number of articles per page (default 10 , maximum support 1000) |

**Note: Request date limit is up to one month**

1. start\_date cannot be less than 30 days from the current date.
2. end\_date cannot be greater than the current date.
3. If no date is passed in, the default query is the reward data of the previous day.

**Example:**start\_date="2023-07-01"end\_date="2023-07-03"The date to be queried is \[2023-07-01, 2023-07-03) left closed right open interval**Response**

| **Parameter name**        | **Data type** | **Description**                                                                                                                   |
| ------------------------- | ------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| date                      | string        | Date (UTC + 8)                                                                                                                    |
| el\_reward                | string        | Execution layer revenue (unit: eth) (real on-chain revenue, if there is a commission ratio, it needs to be calculated separately) |
| cl\_reward                | string        | Consensus layer revenue (unit: eth)                                                                                               |
| total\_reward             | string        | Total revenue of execution layer + consensus layer (unit: eth)                                                                    |
| validators\_active\_count | int           | Number of validators generating revenue                                                                                           |

**Example:**

```JSON
{
    "code": "200",
    "msg": "Success",
    "pagination": {
        "page": 1,
        "limit": 1,
        "total": 2
    },
    "data": {
        "reward": [
            {
                "date": "2023-07-1",
                "el_reward": "0.039144409",
                "cl_reward": "0.0446064811764954",
                "total_reward": "0.0837508901764954",
                "validators_active_count": 2
            },
            {
                "date": "2023-07-2",
                "el_reward": "0.039144409",
                "cl_reward": "0.0446064811764954",
                "total_reward": "0.0837508901764954",
                "validators_active_count": 2
            }
        ]
    }
}

```





## Code

<table data-header-hidden><thead><tr><th width="225"></th><th></th></tr></thead><tbody><tr><td>code</td><td>message</td></tr><tr><td>200</td><td>Success</td></tr><tr><td>400</td><td>Param error</td></tr><tr><td>401</td><td>Authentication failed</td></tr><tr><td>404</td><td>Path Not Found</td></tr><tr><td>500</td><td>Server error</td></tr></tbody></table>
