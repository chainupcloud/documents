# JSON-RPC methods

### Bitcoin RPC

You can review the official[ Bitcoin RPC documentation **HERE**](https://bitcoincore.org/en/doc/24.0.0/rpc/blockchain/getbestblockhash/)**.**&#x20;

### Example RPC

{% tabs %}
{% tab title="Curl" %}
```
curl https://api.chainup.net/bitcoin/mainnet/<YOUR_API_KEY> \
-X POST \
-H 'content-type: application/json' \
--data '{"jsonrpc":"2.0","method":"getblockchaininfo","params":[],"id":1}'
```
{% endtab %}

{% tab title="Javascript" %}
```
const request = require('request');

let options = {
    url: "https://api.chainup.net/bitcoin/mainnet/<YOUR_API_KEY>",
    method: "post",
    headers:
    { 
     "content-type": "application/json"
    },
    body: JSON.stringify({"jsonrpc":"2.0","method":"getblockchaininfo","params":[],"id":1})
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
    "method": "getblockchaininfo",
    "params": []
})
r = requests.post(url="https://api.chainup.net/bitcoin/mainnet/<YOUR_API_KEY>", headers=headers, data=payload)
if r.status_code == 200:
    print("Post successful: response: ", r.content)
else:
    print("An error has occurred: ", r.status_code)
```
{% endtab %}
{% endtabs %}

### **Available  Bitcoin  API request methods**

```
      "getbestblockhash"
      "getblock"
      "getblockchaininfo"
      "getblockcount"
      "getblockfilter"
      "getblockfrompeer"
      "getblockhash"
      "getblockheader"
      "getblockstats"
      "getchaintips"
      "getchaintxstats"
      "getdeploymentinfo"
      "getdifficulty"
      "getmempoolancestors"
      "getmempooldescendants"
      "getmempoolentry"
      "getmempoolinfo"
      "getrawmempool"
      "gettxout"
      "gettxoutproof"
      "gettxoutsetinfo"
      "gettxspendingprevout"
      "preciousblock"
      "pruneblockchain"
      "savemempool"
      "scantxoutset"
      "verifychain"
      "verifytxoutproof"
```

### &#x20;
