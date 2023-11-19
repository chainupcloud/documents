# JSON-RPC methods

### Aptos API

You can review the official Aptos API documentation [**HERE**](https://aptos.dev/nodes/aptos-api-spec/#/)

### Example API

{% tabs %}
{% tab title="Curl" %}
```
curl https://api.chainup.net/aptos/mainnet/<YOUR_API_KEY>/v1/blocks/by_height/1 \
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
    url: "https://api.chainup.net/aptos/mainnet/<YOUR_API_KEY>/v1/blocks/by_height/1",
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
````python
```python
import requests
import json

headers = { "content-type": "application/json",
            "CONSISTENT-HASH": "true" } 
r = requests.get(url="https://api.chainup.net/aptos/mainnet/<YOUR_API_KEY>/v1/blocks/by_height/1", headers=headers)
if r.status_code == 200:
    print("Get successful: response: ", r.content)
else:
    print("An error has occurred: ", r.status_code)
```
````
{% endtab %}
{% endtabs %}
