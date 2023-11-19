# JSON-RPC methods

### Kusama RPC

You can review the official Kusama RPC documentation [**HERE**](https://polkadot.js.org/docs/substrate/rpc/)

### Example RPC

{% tabs %}
{% tab title="Curl" %}
```
curl https://api.chainup.net/kusama/mainnet/<YOUR_API_KEY> \
-X POST \
-H 'content-type: application/json' \
-H "CONSISTENT-HASH: true" \
--data '{"jsonrpc":"2.0","method":"chain_getBlock","params":[],"id":32}'
```
{% endtab %}

{% tab title="Javascript" %}
````javascript
```javascript
const axios = require('axios');
//npm install axios if you don have the module installed`

let options = {
    url: "https://api.chainup.net/kusama/mainnet/<YOUR_API_KEY>",
    method: "post",
    headers:
    { 
     "content-type": "application/json",
     "CONSISTENT-HASH": "true"
    },
    body: JSON.stringify({"jsonrpc":"2.0","method":"chain_getBlock","params":[],"id":32})
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

headers = {"content-type": "application/json",
    "CONSISTENT-HASH": "true" } 
payload = json.dumps({
    "id": 32,
    "jsonrpc": "2.0",
    "method": "chain_getBlock",
    "params": []
})
r = requests.post(url="https://api.chainup.net/kusama/mainnet/<YOUR_API_KEY>", headers=headers, data=payload)
if r.status_code == 200:
    print("Post successful: response: ", r.content)
else:
    print("An error has occurred: ", r.status_code)
```
````
{% endtab %}
{% endtabs %}
