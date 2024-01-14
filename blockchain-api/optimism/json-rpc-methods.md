---
description: >-
  The standard Ethereum methods documented here are supported by Chainup Cloud
  on the Optimism network.
---

# JSON-RPC methods

### **Optimism** RPC

You can review custom methods specific to Optimism can be found in the [**official Optimism API documentation**](https://docs.optimism.io/builders/node-operators/json-rpc)**.**&#x20;

{% hint style="info" %}
Please note that the Optimism Bedrock migration introduces support for various JSON-RPC methods. For detailed information, refer to the [**official Optimism API documentation**](https://docs.optimism.io/builders/node-operators/json-rpc).
{% endhint %}

### Example RPC

{% tabs %}
{% tab title="Curl" %}
<pre><code>curl https://api.chainup.net/optimism/mainnet/&#x3C;YOUR_API_KEY> \
-X POST \
<strong>-H 'content-type: application/json' \
</strong>-H "CONSISTENT-HASH: true" \
--data '{"jsonrpc":"2.0","method":"getblockchaininfo","params":[],"id":1}' 
</code></pre>
{% endtab %}

{% tab title="Javascript" %}
````javascript
```javascript
const axios = require('axios');
//npm install axios if you don have the module installed`

let options = {
url: "https://api.chainup.net/optimism/mainnet/<YOUR_API_KEY>",
method: "post",
headers:
{
"content-type": "application/json",
"CONSISTENT-HASH": "true"
},
body: JSON.stringify({"jsonrpc":"2.0","method":"getblockchaininfo","params":[],"id":1})
};

request(options, (error, response, body) => {
if (error) {
console.error('An error has occurred: ', error);
} else {
console.log('Post successful: response: ', body);
}
});


```
````
{% endtab %}

{% tab title="Python" %}
```python
import requests
import json

headers = {"content-type": "application/json",
            "CONSISTENT-HASH": "true" } 
payload = json.dumps({
"id": 1,
"jsonrpc": "2.0",
"method": "getblockchaininfo",
"params": []
})
r = requests.post(url="https://api.chainup.net/optimism/mainnet/<YOUR_API_KEY>", headers=headers, data=payload)
if r.status_code == 200:
print("Post successful: response: ", r.content)
else:
print("An error has occurred: ", r.status_code)
```
{% endtab %}
{% endtabs %}
