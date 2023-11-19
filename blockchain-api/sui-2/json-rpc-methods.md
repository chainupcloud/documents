# JSON-RPC methods

### Cosmos RPC

You can review the official [**Cosmos API documentation HERE.** ](https://docs.cosmos.network/swagger/)

### Example RPC

{% tabs %}
{% tab title="Curl" %}
<pre><code>curl https://api.chainup.net/cosmos/mainnet/&#x3C;YOUR_API_KEY> \
-X POST \
<strong>-H 'content-type: application/json' \
</strong>-H "CONSISTENT-HASH: true" \
--data '{"jsonrpc":"2.0","method":"/node_info","params":[],"id":1}' 
</code></pre>
{% endtab %}

{% tab title="Javascript" %}
````javascript
```javascript
const axios = require('axios');
//npm install axios if you don have the module installed`

let options = {
    url: "https://api.chainup.net/cosmos/mainnet/<YOUR_API_KEY>",
    method: "post",
    headers:
    { 
     "content-type": "application/json",
     "CONSISTENT-HASH": "true"
    },
    body: JSON.stringify({"jsonrpc":"2.0","method":"node_info","params":[],"id":1})
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
    "method": "node_info",
    "params": []
})
r = requests.post(url="https://api.chainup.net/cosmos/mainnet/<YOUR_API_KEY>", headers=headers, data=payload)
if r.status_code == 200:
    print("Post successful: response: ", r.content)
else:
    print("An error has occurred: ", r.status_code)
```
````
{% endtab %}
{% endtabs %}
