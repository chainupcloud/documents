# JSON-RPC methods

### **Dogecoin** RPC

You can review the official [**Dogecoin API documentation HERE**](https://docs.dogechain.dog/docs/get-started/json-rpc-commands)**.**&#x20;

### Example RPC

{% tabs %}
{% tab title="Curl" %}
<pre><code>curl https://api.chainup.net/dogecoin/mainnet/&#x3C;YOUR_API_KEY> \
-X POST \
<strong>-H 'content-type: application/json' \
</strong>--data '{"jsonrpc":"2.0","method":"getpeerinfo","params":[],"id":32}'
</code></pre>
{% endtab %}

{% tab title="Javascript" %}
```
const request = require('request');

let options = {
url: "https://api.chainup.net/dogecoin/mainnet/<YOUR_API_KEY>",
method: "post",
headers:
{
"content-type": "application/json"
},
body: JSON.stringify({"jsonrpc":"2.0","method":"getpeerinfo","params":[],"id":1})
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
"method": "getpeerinfo",
"params": []
})
r = requests.post(url="https://api.chainup.net/dogecoin/mainnet/<YOUR_API_KEY>", headers=headers, data=payload)
if r.status_code == 200:
print("Post successful: response: ", r.content)
else:
print("An error has occurred: ", r.status_code)
```
{% endtab %}
{% endtabs %}
