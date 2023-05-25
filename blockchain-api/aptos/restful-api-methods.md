# RESTful API methods

### Aptos API

You can review the official Aptos API documentation [**HERE**](https://aptos.dev/nodes/aptos-api-spec/#/)

### Example API

{% tabs %}
{% tab title="Curl" %}
```
curl https://api.chainup.net/aptos/mainnet/<YOUR_API_KEY>/v1/blocks/by_height/1 \
-X GET \
-H 'content-type: application/json' 
```
{% endtab %}

{% tab title="Javascript" %}
```
const request = require('request');

let options = {
    url: "https://api.chainup.net/aptos/mainnet/<YOUR_API_KEY>/v1/blocks/by_height/1",
    method: "get",
    headers:
    { 
     "content-type": "application/json"
    }
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
r = requests.get(url="https://api.chainup.net/aptos/mainnet/<YOUR_API_KEY>/v1/blocks/by_height/1", headers=headers)
if r.status_code == 200:
    print("Get successful: response: ", r.content)
else:
    print("An error has occurred: ", r.status_code)
```
{% endtab %}
{% endtabs %}
