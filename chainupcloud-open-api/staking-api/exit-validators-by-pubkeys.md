---
description: Unstake ETH from multiple validators at once.
---

# Exit Validators by Pubkeys

**HTTP Request**

```HTTP
POST /api/v1/validator/exit
```

**Path Params**No param\
**Request Params**

| **Parameter name** | **Data type** | **Whether it must be passed.** | **Description** |
| ------------------ | ------------- | ------------------------------ | --------------- |
| pubkeys            | array         | true                           | Verifier list   |

\
**Response**None\
**Example**

```JSON
{
    "code": "200",
    "msg": "Success"
}
```

\
\
\
