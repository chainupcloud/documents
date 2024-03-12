---
description: >-
  Broadcast a signed staking transaction. Returns a transaction hash whose
  status can be checked using the Ethereum RPC eth_getTransactionReceipt method
  (reference).
---

# Broadcast Staking Tx

### **HTTP Request**

This API allows the broadcasting of a signed staking transaction.

```HTTP
POST /api/v1/validator/broadcast
```

**Path Params:** No parameters

**Request Params:**

* **signed\_transaction (string) \[Required]:** The signed staking transaction.

<table data-header-hidden><thead><tr><th width="229"></th><th></th><th></th><th></th></tr></thead><tbody><tr><td><strong>Parameter name</strong></td><td><strong>Data type</strong></td><td><strong>Whether it must be passed.</strong></td><td><strong>Description</strong></td></tr><tr><td>signed_transaction</td><td>string</td><td>true</td><td>Signed tx</td></tr></tbody></table>



**Response:**

* Upon successful broadcasting, the response contains a transaction hash (`tx_hash`) for the deposited transaction.
* **tx\_hash (string):** Hash of the deposited transaction.

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

**Response Explanation:**

* In this example, the HTTP response code is `200`, indicating success. The `tx_hash` in the data field represents the hash of the deposited staking transaction.
