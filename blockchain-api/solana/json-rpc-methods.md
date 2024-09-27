# JSON-RPC methods

### Solana RPC



At Chainup Cloud, we manage Solana RPC endpoints, handling hundreds of billions of requests each month. To simplify integration for developers, we've created documentation with examples of how to call RPC methods using cURL, JavaScript, Python.  Chainup Cloudsupports a wide range of Solana APIs, making development easier and more efficient.

<figure><img src="../../.gitbook/assets/image (89).png" alt=""><figcaption></figcaption></figure>

You can review the official [**Solana RPC documentation HERE**](https://solana.com/docs/rpc)

### Example RPC

{% tabs %}
{% tab title="Curl" %}
```
curl   https://api.chainup.net/solana/mainnet/<YOUR_API_KEY>  \
-X POST \
-H "Content-Type: application/json" \
--data '{"jsonrpc": "2.0","id": 1,"method": "getAccountInfo","params": ["7cVfgArCheMR6Cs4t6vz5rfnqd56vZq4ndaBrY5xkxXy",{"encoding": "base58"}]}'
```
{% endtab %}

{% tab title="Javascript" %}
<pre class="language-javascript"><code class="lang-javascript"><strong>const axios = require('axios');
</strong>//npm install axios if you don have the module installed`
let options = {
    url: "https://api.chainup.net/solana/mainnet/&#x3C;YOUR_API_KEY>",
    method: "post",
    headers:
    { 
     "content-type": "application/json"
    },
    body: JSON.stringify({"jsonrpc": "2.0","id": 1,"method": "getAccountInfo","params": ["7cVfgArCheMR6Cs4t6vz5rfnqd56vZq4ndaBrY5xkxXy",{"encoding": "base58"}])
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

# Set the headers for the request
headers = {
    "Content-Type": "application/json",
    "CONSISTENT-HASH": "true"
}

# Prepare the payload for the RPC request
payload = json.dumps({
    "jsonrpc": "2.0",
    "id": 1,
    "method": "getAccountInfo",
    "params": [
        "7cVfgArCheMR6Cs4t6vz5rfnqd56vZq4ndaBrY5xkxXy",
        {"encoding": "base58"}
    ]
})

# Send the POST request to the Solana RPC endpoint
url = "https://api.chainup.net/solana/mainnet/<YOUR_API_KEY>"

try:
    r = requests.post(url=url, headers=headers, data=payload)
    # Check if the request was successful
    if r.status_code == 200:
        print("Post successful: response: ", r.content)
    else:
        print(f"An error occurred: {r.status_code}")
except requests.exceptions.RequestException as e:
    print(f"Request failed: {e}")

```
{% endtab %}
{% endtabs %}
