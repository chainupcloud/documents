# JSON-RPC methods

### Arbitrum RPC

You can review the official[ Arbitrum API documentation **HERE.** ](https://arbiscan.io/apis#contracts)

### Example RPC

{% tabs %}
{% tab title="Curl" %}
```
curl https://api.chainup.net/arbitrum/mainnet/<YOUR_API_KEY> \
-X POST \
-H 'content-type: application/json' \
-H "CONSISTENT-HASH: true" \
--data '{"jsonrpc":"2.0","method":"eth_syncing","params":[],"id":1}' 
```
{% endtab %}

{% tab title="Javascript" %}
````
```javascript

const axios = require('axios');
//npm install axios if you don have the module installed`

let options = {
    // url: "https://api.chainup.net/arbitrum/mainnet/<YOUR_API_KEY>",
    url: "https://api.chainup.net/arbitrum/mainnet/dc59a7e90f05424a81d825d033d0f2de",
    method: "post",
    headers:
    { 
     "content-type": "application/json",
     "CONSISTENT-HASH": "true"
    },
    body: JSON.stringify({"jsonrpc":"2.0","method":"eth_syncing","params":[],"id":1})
};

axios(options)
.then(response => {
console.log('Post successful: response:', response.data);
})
.catch(error => {
console.error('An error has occurred:', error);
});
```
````
{% endtab %}

{% tab title="Python" %}
````python
```python
import requests
import json

headers = {"content-type": "application/json" ,
            "CONSISTENT-HASH": "true" } 
payload = json.dumps({
    "id": 1,
    "jsonrpc": "2.0",
    "method": "eth_syncing",
    "params": []
})
r = requests.post(url="https://api.chainup.net/arbitrum/mainnet/<YOUR_API_KEY>", headers=headers, data=payload)
if r.status_code == 200:
    print("Post successful: response: ", r.content)
else:
    print("An error has occurred: ", r.status_code)
```
````
{% endtab %}
{% endtabs %}
