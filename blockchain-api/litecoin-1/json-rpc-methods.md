# JSON-RPC methods

### Litecoin RPC

You can review the official Litecoin RPC documentation [**HERE**](https://litecoin.info/index.php/Litecoin\_API)

### Example RPC

{% tabs %}
{% tab title="Curl" %}
<pre><code><strong>curl https://api.chainup.net/near/mainnet/&#x3C;YOUR_API_KEY> \
</strong>-X POST \
-H 'content-type: application/json' \
---data '{"jsonrpc":"2.0","method":"network_info","params":[],"id":1}'  
</code></pre>
{% endtab %}

{% tab title="Javascript" %}
```
const request = require('request');

let options = {
    url: "https://api.chainup.net/near/mainnet/<YOUR_API_KEY>",
    method: "post",
    headers:
    { 
     "content-type": "application/json"
    },
    body: JSON.stringify({"jsonrpc":"2.0","method":"network_info","params":[],"id":1})
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
    "id": 1,
    "jsonrpc": "2.0",
    "method": "network_info",
    "params": []
})
r = requests.post(url="https://api.chainup.net/near/mainnet/<YOUR_API_KEY>", headers=headers, data=payload)
if r.status_code == 200:
    print("Post successful: response: ", r.content)
else:
    print("An error has occurred: ", r.status_code)
```
{% endtab %}
{% endtabs %}
