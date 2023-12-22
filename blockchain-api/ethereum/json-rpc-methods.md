# JSON-RPC methods

### Example RPC

{% tabs %}
{% tab title="Curl" %}
```
curl https://api.chainup.net/ethereum/mainnet/<YOUR_API_KEY> \
-X POST \
-H 'content-type: application/json' \
-H "CONSISTENT-HASH: true" \
--data '{"jsonrpc":"2.0","method":"net_peerCount","params":[],"id":1}' 
```
{% endtab %}

{% tab title="Javascript" %}
```
const axios = require('axios'); 
//npm install axios if you don have the module installed

let options = {
    url: "https://api.chainup.net/ethereum/mainnet/<YOUR_API_KEY>",
    method: "post",
    headers: {
        "content-type": "application/json",
        "CONSISTENT-HASH": "true"  // Add your custom header here
    },
    data: {"jsonrpc":"2.0","method":"net_peerCount","params":[],"id":1}
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
```python
import requests
import json

headers = {
    "content-type": "application/json",
    "CONSISTENT-HASH": "true"  # Add your custom header here
}

payload = json.dumps({
    "id": 1,
    "jsonrpc": "2.0",
    "method": "net_peerCount",
    "params": []
})

url = "https://api.chainup.net/ethereum/mainnet/00164210c0334c76a235aca8b1dcf655"
r = requests.post(url=url, headers=headers, data=payload)

if r.status_code == 200:
    print("Post successful: response: ", r.content)
else:
    print("An error has occurred: ", r.status_code)

```
{% endtab %}
{% endtabs %}

### Ethereum RPC

You can review the official Ethereum RPC documentation [**HERE**](https://ethereum.org/en/developers/docs/apis/json-rpc/)

**Available Ethereum API request methods**

```solidity
          "eth_accounts"
          "eth_blockNumber"
          "eth_call"
          "eth_chainId"
          "eth_freeHistory"
          "eth_getBalance"
          "eth_getBlockByHash"
          "eth_getBlockByNumber"
          "eth_getBlockTransactionCountByHash"
          "eth_getBlocTransactionCountByNumber"
          "eth_getCode"
          "eth_getFilterChanges"
          "eth_getFilterLogs"
          "eth_getLogs"
          "eth_getStorageAt"
          "eth_getTransactionByHash"
          "eth_getTransactionByCount"
          "eth_getTransactionHashByCid"
          "eth_getTransactionReceipt"
          "eth_maxPriorityFeePerGas"
          "eth_newBlockFilter"
          "eth_newPendingTransactionFilter"
          "eth_sendRawTransaction"
          "eth_uninstallFilter"
          "eth_requestAccounts"
          "eth_sendTransaction"
          "eth_sign"
          "eth_gasPrice"
          "eth_estimateGas"
          "net_version"
```

{% hint style="info" %}
Due to the computational resources consumed by certain RPCs, the free public RPC only supports the RPCs mentioned above. The rest of the JSON-RPCs will be intercepted and return a 403 status code.
{% endhint %}

{% hint style="info" %}
We only collect user IP addresses for the purpose of rate limiting. For more information, please visit: [https://www.chainup.com/privacyPolicy](https://www.chainup.com/privacyPolicy)
{% endhint %}
