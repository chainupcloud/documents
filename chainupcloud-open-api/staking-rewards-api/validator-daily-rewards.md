# Validator Daily  Rewards

#### Validator Daily Rewards

**Query the daily rewards within the specified date of the user verifierHTTP Request**

```HTTP
Get /api/v1/validator/daliy-rewards
```

**Path Params**No param\
**Request Params**

| **Parameter name** | **Data type** | **Whether it must be passed.** | **Description**                                                      |
| ------------------ | ------------- | ------------------------------ | -------------------------------------------------------------------- |
| start\_date        | string        | false                          | Start date (YYYY-MM-DD) (UTC + 8)                                    |
| end\_date          | string        | false                          | End date (YYYY-MM-DD) (UTC + 8)                                      |
| page               | int           | false                          | Page number (default is 1)                                           |
| limit              | int           | false                          | Number of entries per page (default is 10 , maximum support is 1000) |

**Note: Request date limit is up to one month**

1. start\_date cannot be less than 30 days from the current date.
2. end\_date cannot be greater than the current date.
3. If no date is passed in, the default query is the reward data of the previous day.

**Example:**start\_date="2023-07-01"end\_date="2023-07-03"The date to be queried is \[2023-07-01, 2023-07-03) Left closed right open interval**Response**

| **Parameter name**        | **Data type** | **Description**                                                                                                             |
| ------------------------- | ------------- | --------------------------------------------------------------------------------------------------------------------------- |
| date                      | string        | Date (UTC + 8)                                                                                                              |
| el\_reward                | string        | Execution layer income (unit: eth) (real income on the chain, if there is settlement, it needs to be calculated separately) |
| cl\_reward                | string        | Consensus layer revenue (unit: eth)                                                                                         |
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
