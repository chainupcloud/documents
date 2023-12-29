# JSON-RPC methods

### Filecoin RPC

You can review the official Filecoin RPC documentation [**HERE**](https://lotus.filecoin.io/reference/basics/overview/)

{% hint style="info" %}
Due to the computational resources consumed by certain RPCs, the free public RPC only supports the RPCs mentioned above. The rest of the JSON-RPCs will be intercepted and return a 403 status code.
{% endhint %}

{% hint style="info" %}
We only collect user IP addresses for the purpose of rate limiting. For more information, please visit: [https://www.chainup.com/privacyPolicy](https://www.chainup.com/privacyPolicy)
{% endhint %}

### Example RPC

{% tabs %}
{% tab title="Curl" %}
```
curl https://api.chainup.net/filecoin/mainnet/<YOUR_API_KEY> \
-X POST \
-H 'content-type: application/json' \
-H "CONSISTENT-HASH: true" \
--data '{"jsonrpc":"2.0","method":"Filecoin.Version","params":[],"id":1}'
```
{% endtab %}

{% tab title="Javascript" %}
```
const axios = require('axios');
//npm install axios if you don have the module installed

let options = {
url: "https://api.chainup.net/filecoin/mainnet/<YOUR_API_KEY>/rpc/v1",
method: "post",
headers:
{
"content-type": "application/json",
"CONSISTENT-HASH": "true"
},
body: JSON.stringify({"jsonrpc":"2.0","method":"Filecoin.Version","params":[],"id":1})
};

axios(options)
.then(response => {
console.log('Post successful: response:', response.data);
})
.catch(error => {
console.error('An error has occurred:', error);
});
```
{% endtab %}

{% tab title="Python" %}
````
```python
import requests
import json

headers = {"content-type": "application/json",
    "CONSISTENT-HASH": "true" }
payload = json.dumps({
    "id": 1,
    "jsonrpc": "2.0",
    "method": "Filecoin.Version",
    "params": []
})
r = requests.post(url="https://api.chainup.net/filecoin/mainnet/<YOUR_API_KEY>/rpc/v1", headers=headers, data=payload)
if r.status_code == 200:
    print("Post successful: response: ", r.content)
else:
    print("An error has occurred: ", r.status_code)
```
````
{% endtab %}
{% endtabs %}
