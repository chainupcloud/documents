---
description: Query the daily rewards within the specified date of the user verifier
---

# Validator Daily  Rewards

### **HTTP Request**

* This API allows querying daily rewards for a user verifier within a specified date range.

```HTTP
Get /api/v1/validator/daliy-rewards
```

**Path Params:** No parameters



### **Request Params**

* `start_date` (Optional): Start date for querying rewards.
* `end_date` (Optional): End date for querying rewards.

| **Parameter name** | **Data type** | **Whether it must be passed.** | **Description**                                                      |
| ------------------ | ------------- | ------------------------------ | -------------------------------------------------------------------- |
| start\_date        | string        | false                          | Start date (YYYY-MM-DD) (UTC + 8)                                    |
| end\_date          | string        | false                          | End date (YYYY-MM-DD) (UTC + 8)                                      |
| page               | int           | false                          | Page number (default is 1)                                           |
| limit              | int           | false                          | Number of entries per page (default is 10 , maximum support is 1000) |

### **Note on Request Params:**

* If no date is provided, the default query is for the reward data of the previous day.
* The example request queries rewards for the date range \[2023-07-01, 2023-07-03), a left-closed right-open interval.

### **Example Request:**

```bash
GET /api/v1/validator/daily-rewards?start_date=2023-07-01&end_date=2023-07-03

```

### **Response**

| **Parameter name**        | **Data type** | **Description**                                                                                                             |
| ------------------------- | ------------- | --------------------------------------------------------------------------------------------------------------------------- |
| date                      | string        | Date (UTC + 8)                                                                                                              |
| el\_reward                | string        | Execution layer income (unit: eth) (real income on the chain, if there is settlement, it needs to be calculated separately) |
| cl\_reward                | string        | Consensus layer revenue (unit: eth)                                                                                         |
| total\_reward             | string        | Total revenue of execution layer + consensus layer (unit: eth)                                                              |
| validators\_active\_count | int           | Number of validators generating revenue                                                                                     |

### **Response:**

* The response code is `200`, indicating success.
* The `pagination` field provides information about the page, limit, and total records.
* The `data` field contains an array of daily rewards, each with details such as date, el\_reward, cl\_reward, total\_reward, and validators\_active\_count.

### **Example:**

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
