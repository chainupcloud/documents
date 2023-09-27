# ⚖ Staking API

### Base URL & Auth

http://staking.chainup.net/${protocol}/mainnet/${token}\
**Supporting Protocol**

| Protocol | Network |
| -------- | ------- |
| Ethereum | Mainnet |

\
**Path Params**

<table data-header-hidden><thead><tr><th></th><th></th><th width="160"></th><th></th></tr></thead><tbody><tr><td><strong>Parameter Name</strong></td><td><strong>Data Type</strong></td><td><strong>Mandatory</strong></td><td><strong>Description</strong></td></tr><tr><td>protocol</td><td>string</td><td>true</td><td>Protocol(ethereum)</td></tr><tr><td>token</td><td>string</td><td>true</td><td>The user is bound to the Staking token and authenticated through the token.</td></tr></tbody></table>

\
**Create token**

1. ChainUp creates a token and sends it to the customer via email.
2. The client generates token.\


### ETH Staking API

> Only the validators of the ChainUpCloud platform are counted.

#### Validator Total Rewards

**Query the user’s historical cumulative rewards for validators**\
**HTTP Request**

```HTTP
Get /api/v1/validator/total-rewards
```

**Path Params:** No param\
**Request Params**

<table data-header-hidden><thead><tr><th></th><th></th><th width="154"></th><th></th></tr></thead><tbody><tr><td><strong>Parameter Name</strong></td><td><strong>Data Type</strong></td><td><strong>Mandatory</strong></td><td><strong>Description</strong></td></tr><tr><td>page</td><td>int</td><td>false</td><td>Page number (default is 1)</td></tr><tr><td>limit</td><td>int</td><td>false</td><td>Number of items per page (default is 10, maximum supported is 1000)</td></tr></tbody></table>

\
**Response**

<table data-header-hidden><thead><tr><th></th><th width="184.33333333333331"></th><th></th></tr></thead><tbody><tr><td><strong>Parameter Name</strong></td><td><strong>Data Type</strong></td><td><strong>Description</strong></td></tr><tr><td>el_total_reward</td><td>string</td><td>Total revenue of the execution layer (unit: eth) (real revenue on the chain, if there is settlement, it needs to be calculated separately)</td></tr><tr><td>cl_total_reward</td><td>string</td><td>Total income of the consensus layer (unit: eth)</td></tr><tr><td>total_reward</td><td>string</td><td>Total revenue of execution layer + consensus layer (unit: eth)</td></tr><tr><td>cl_balance</td><td>string</td><td>Consensus layer balance (unit: eth)</td></tr><tr><td>status</td><td>string</td><td>Validator status</td></tr><tr><td>validators_active_count</td><td>int</td><td>Number of active validators</td></tr><tr><td>validators_total_count</td><td>int</td><td>Total number of validators</td></tr><tr><td>validators_total_rewards</td><td>string</td><td>Accumulated total rewards for validators</td></tr><tr><td>validators_total_cl_balance</td><td>string</td><td>Total balance of validator consensus layer</td></tr></tbody></table>

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

\


#### Validator Daily Rewards

Query the daily rewards of user verifiers within the specified date **(HTTP Request)**

```HTTP
Get /api/v1/validator/daliy-rewards
```

**Path Params:** No param\
**Request Params**

<table data-header-hidden><thead><tr><th></th><th width="129"></th><th width="148"></th><th></th></tr></thead><tbody><tr><td><strong>Parameter Name</strong></td><td><strong>Data Type</strong></td><td><strong>Mandatory</strong></td><td><strong>Description</strong></td></tr><tr><td>start_date</td><td>string</td><td>false</td><td>Start date (YYYY-MM-DD) (UTC+8)</td></tr><tr><td>end_date</td><td>string</td><td>false</td><td>End date (YYYY-MM-DD) (UTC+8)</td></tr><tr><td>page</td><td>int</td><td>false</td><td>Page number (default is 1)</td></tr><tr><td>limit</td><td>int</td><td>false</td><td>Number of items per page (default is 10, maximum supported is 1000)</td></tr></tbody></table>

**Note: Request date limit is one month at most**

1. start\_date cannot be less than the current date -30 days.
2. end\_date cannot be greater than the current date.
3. If no date is passed in, the reward data of the previous day will be queried by default.

**Example** :start\_date="2023-07-01"end\_date="2023-07-03"The date to be queried is \[2023-07-01, 2023-07-03) left closed and right open interval  \
\
**Response**&#x20;

| **Parameter Name**        | **Data Type** | **Description**                                                                                                             |
| ------------------------- | ------------- | --------------------------------------------------------------------------------------------------------------------------- |
| date                      | string        | Date (UTC+8)                                                                                                                |
| el\_reward                | string        | Execution layer income (unit: eth) (real income on the chain, if there is settlement, it needs to be calculated separately) |
| cl\_reward                | string        | Consensus layer income (unit: eth)                                                                                          |
| total\_reward             | string        | Total revenue of execution layer + consensus layer (unit: eth)                                                              |
| validators\_active\_count | int           | Number of validators generating revenue                                                                                     |

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

| code | message                            |
| ---- | ---------------------------------- |
| 200  | Success                            |
| 400  | Param error                        |
| 401  | Authentication failed              |
| 404  | Path Not Found                     |
| 500  | Server error                       |
| 4001 | Date format is incorrect           |
| 4002 | Date can not be greater than today |
| 4003 | Only support nearly 30 reward data |

\
