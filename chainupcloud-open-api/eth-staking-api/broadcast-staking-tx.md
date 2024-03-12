---
description: >-
  Broadcast a signed staking transaction. Returns a transaction hash whose
  status can be checked using the Ethereum RPC eth_getTransactionReceipt method
  (reference).
---

# Broadcast Staking Tx

**HTTP Request**

```HTTP
POST /api/v1/validator/broadcast
```

**Path Params**No param\
**Request Params**

| **Parameter name**  | **Data type** | **Whether it must be passed.** | **Description** |
| ------------------- | ------------- | ------------------------------ | --------------- |
| signed\_transaction | string        | true                           | Signed tx       |

\
**Response**

| **Parameter name** | **Data type** | **Description** |
| ------------------ | ------------- | --------------- |
| tx\_hash           | string        | Deposit tx hash |

\
**Example**

```JSON
{
    "code": "200",
    "msg": "Success",
    "data": {
        "tx_hash": "0xae96cb28f012f20a63118cf34f60de63c9884a483cc742d5f41a1aee6f5cd5f3"
    }
}
```
