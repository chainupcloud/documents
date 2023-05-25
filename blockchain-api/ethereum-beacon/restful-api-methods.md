# RESTful API methods

### Ethereum Beacon API

You can review the official Ethereum Beacon API documentation [**HERE**](https://ethereum.github.io/beacon-APIs/?urls.primaryName=dev#/Beacon)

### Example API

{% tabs %}
{% tab title="Curl" %}
```
curl https://api.chainup.net/ethereum2/mainnet/<YOUR_API_KEY>/eth/v1/node/syncing \
-X GET \
-H 'content-type: application/json' 
```
{% endtab %}

{% tab title="Javascript" %}
```
const request = require('request');

let options = {
    url: "https://api.chainup.net/ethereum2/mainnet/<YOUR_API_KEY>/eth/v1/node/syncing",
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
r = requests.get(url="https://api.chainup.net/ethereum2/mainnet/<YOUR_API_KEY>/eth/v1/node/syncing", headers=headers)
if r.status_code == 200:
    print("Get successful: response: ", r.content)
else:
    print("An error has occurred: ", r.status_code)
```
{% endtab %}
{% endtabs %}
