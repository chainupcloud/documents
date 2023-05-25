# RESTful API methods

### EOS API

You can review the official EOS API documentation [**HERE**](https://developers.eos.io/manuals/eos/latest/nodeos/plugins/chain\_api\_plugin/api-reference/index)

### Example API

{% tabs %}
{% tab title="Curl" %}
```
curl https://api.chainup.net/eos/mainnet/<YOUR_API_KEY>/v1/chain/get_info \
-X GET \
-H 'content-type: application/json' 
```
{% endtab %}

{% tab title="Javascript" %}
```
const request = require('request');

let options = {
    url: "https://api.chainup.net/eos/mainnet/<YOUR_API_KEY>/v1/chain/get_info",
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
r = requests.get(url="https://api.chainup.net/eos/mainnet/<YOUR_API_KEY>/v1/chain/get_info", headers=headers)
if r.status_code == 200:
    print("Get successful: response: ", r.content)
else:
    print("An error has occurred: ", r.status_code)
```
{% endtab %}
{% endtabs %}
