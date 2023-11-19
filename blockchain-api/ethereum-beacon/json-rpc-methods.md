# JSON-RPC methods

### Ethereum Beacon API

You can review the official Ethereum Beacon API documentation [**HERE**](https://ethereum.github.io/beacon-APIs/?urls.primaryName=dev#/Beacon)

### Example API

{% tabs %}
{% tab title="Curl" %}
```
curl https://api.chainup.net/ethereum2/mainnet/<YOUR_API_KEY>/eth/v1/node/syncing \
-X GET \
-H 'content-type: application/json' \
-H "CONSISTENT-HASH: true" 
```
{% endtab %}

{% tab title="Javascript" %}
```javascript
const axios = require('axios');
//npm install axios if you don have the module installed`

let options = {
    url: "https://api.chainup.net/ethereum2/mainnet/<YOUR_API_KEY>/eth/v1/node/syncing",
    method: "get",
    headers:
    { 
     "content-type": "application/json",
     "CONSISTENT-HASH": "true"
    }
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
<pre class="language-python"><code class="lang-python">
<strong>import requests
</strong>import json

headers = {"content-type": "application/json",
    "CONSISTENT-HASH": "true"}
r = requests.get(url="https://api.chainup.net/ethereum2/mainnet/&#x3C;YOUR_API_KEY>/eth/v1/node/syncing", headers=headers)
if r.status_code == 200:
    print("Get successful: response: ", r.content)
else:
    print("An error has occurred: ", r.status_code)

</code></pre>
{% endtab %}
{% endtabs %}
