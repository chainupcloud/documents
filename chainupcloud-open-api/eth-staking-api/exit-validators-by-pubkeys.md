---
description: Unstake ETH from multiple validators at once.
---

# Exit Validators by Pubkeys

This API endpoint allows you to **unstake** from multiple validators **simultaneously**.

### **HTTP Request**

```HTTP
POST /api/v1/validator/exit
```

**Path Params**

No param\


**Request:**

* **pubkeys (array):** This parameter is mandatory and requires a list of public keys for the validators you want to exit.

### **Response:**

* If successful, you'll receive a response with:
  * **code:** "200" indicating success.
  * **msg:** "Success" confirming the exit request.

### Example

```JSON
{
    "code": "200",
    "msg": "Success"
}

```

{% hint style="info" %}
* This API simplifies the process of exiting from several validators compared to exiting them individually.
* Double-check the public keys to ensure you're targeting the intended validators.
{% endhint %}
