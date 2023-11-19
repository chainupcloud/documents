# JSON-RPC methods

### EOS API

You can review the official EOS API documentation [**HERE**](https://developers.eos.io/manuals/eos/latest/nodeos/plugins/chain\_api\_plugin/api-reference/index)

### Example API

{% tabs %}
{% tab title="Curl" %}
```
curl https://api.chainup.net/eos/mainnet/<YOUR_API_KEY>/v1/chain/get_info \
-X GET \
-H 'content-type: application/json'
-H "CONSISTENT-HASH: true" \
```
{% endtab %}

{% tab title="Javascript" %}
````javascript
```javascript
const axios = require('axios');
//npm install axios if you don have the module installed`

let options = {
    url: "https://api.chainup.net/eos/mainnet/<YOUR_API_KEY>/v1/chain/get_info",
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
````
{% endtab %}

{% tab title="Python" %}
```python
import requests
import json

headers = {"content-type": "application/json"  ,
    "CONSISTENT-HASH": "true" } 
r = requests.get(url="https://api.chainup.net/eos/mainnet/<YOUR_API_KEY>/v1/chain/get_info", headers=headers)
if r.status_code == 200:
    print("Get successful: response: ", r.content)
else:
    print("An error has occurred: ", r.status_code)
```
{% endtab %}
{% endtabs %}
