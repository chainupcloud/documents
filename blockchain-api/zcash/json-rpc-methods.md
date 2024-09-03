# JSON-RPC methods

### Zcash RPC

You can review the official[ **Zcash RPC documentation HERE**](https://zcash.github.io/rpc/)

### Example RPC

{% tabs %}
{% tab title="Curl" %}
<pre><code><strong>curl https://api.chainup.net/zcash/mainnet/&#x3C;YOUR_API_KEY> \
</strong>-X POST \
-H 'content-type: application/json' \
-H "CONSISTENT-HASH: true" \
---data '{"jsonrpc":"2.0","method":"getblock","params":[],"id":1}'  
</code></pre>
{% endtab %}

{% tab title="Javascript" %}
<pre class="language-javascript"><code class="lang-javascript"><strong>const axios = require('axios');
</strong>//npm install axios if you don have the module installed`
let options = {
    url: "https://api.chainup.net/dash/mainnet/&#x3C;YOUR_API_KEY>",
    method: "post",
    headers:
    { 
     "content-type": "application/json"
    },
    body: JSON.stringify({"jsonrpc":"2.0","method":"getgovernanceinfo","params":[],"id":1})
};

axios(options)
.then(response => {
console.log('Post successful: response:', response.data);
})
.catch(error => {
console.error('An error has occurred:', error);
});
</code></pre>
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
    "method": "getgovernanceinfo",
    "params": []
})
r = requests.post(url="https://api.chainup.net/dash/mainnet/<YOUR_API_KEY>", headers=headers, data=payload)
if r.status_code == 200:
    print("Post successful: response: ", r.content)
else:
    print("An error has occurred: ", r.status_code)
```
{% endtab %}
{% endtabs %}
