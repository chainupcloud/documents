# JSON-RPC methods

### Polkadot RPC

You can review the official Polkadot RPC documentation [**HERE**](https://polkadot.js.org/docs/substrate/rpc/)

### Example RPC

{% tabs %}
{% tab title="Curl" %}
```
curl https://api.chainup.net/polkadot/mainnet/<YOUR_API_KEY> \
-X POST \
-H 'content-type: application/json' \
-H "CONSISTENT-HASH: true" \
--data '{"jsonrpc":"2.0","method":"chain_getBlock","params":[],"id":32}'
```
{% endtab %}

{% tab title="Javascript" %}
```
const request = require('request');

let options = {
    url: "https://api.chainup.net/polkadot/mainnet/<YOUR_API_KEY>",
    method: "post",
    headers:
    { 
     "content-type": "application/json"
    },
    body: JSON.stringify({"jsonrpc":"2.0","method":"chain_getBlock","params":[],"id":32})
};

request(options, (error, response, body) => {
    if (error) {
        console.error('An error has occurred: ', error);
    } else {
        console.log('Post successful: response: ', body);
    }
});
```
{% endtab %}

{% tab title="Python" %}
```
import requests
import json

headers = {"content-type": "application/json"}
payload = json.dumps({
    "id": 32,
    "jsonrpc": "2.0",
    "method": "chain_getBlock",
    "params": []
})
r = requests.post(url="https://api.chainup.net/polkadot/mainnet/<YOUR_API_KEY>", headers=headers, data=payload)
if r.status_code == 200:
    print("Post successful: response: ", r.content)
else:
    print("An error has occurred: ", r.status_code)
```
{% endtab %}
{% endtabs %}
