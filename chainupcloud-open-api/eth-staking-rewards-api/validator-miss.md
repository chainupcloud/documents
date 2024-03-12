# Validator  Miss

**Query the accumulated misses of user authenticator within the specified date.HTTP Request**

```HTTP
Get /api/v1/validator/miss
```

**Path Params**No param\
**Request Params**

| **Parameter name** | **Data type** | **Whether it must be passed.** | **Description**                   |
| ------------------ | ------------- | ------------------------------ | --------------------------------- |
| start\_date        | string        | false                          | Start date (YYYY-MM-DD) (UTC + 8) |
| end\_date          | string        | false                          | End date (YYYY-MM-DD) (UTC + 8)   |

**Note: Request date limit is up to one month**

1. start\_date cannot be less than 30 days from the current date.
2. end\_date cannot be greater than the current date.
3. If no date is passed in, the missing data of the previous day will be queried by default.

\
**Response**

| **Parameter name** | **Data type** | **Description**                   |
| ------------------ | ------------- | --------------------------------- |
| miss\_count        | int           | Number of missing                 |
| miss\_amount       | string        | Missing amount (unit: wei)        |
| start\_date        | string        | Start date (YYYY-MM-DD) (UTC + 8) |
| end\_date          | string        | End date (YYYY-MM-DD) (UTC + 8)   |

**Example:**

```JSON
{
    "code": "200",
    "msg": "Success",
    "data": {
        "start_date": "2023-07-01",
        "end_date": "2023-07-30",
        "miss_count": 1,
        "miss_amount": "51000000000000000"
    }
}
```
