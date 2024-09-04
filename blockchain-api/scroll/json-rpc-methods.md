# JSON-RPC methods

### Scroll RPC

You can review the official [**Scroll RPC documentation HERE**](https://docs.scroll.io/en/developers/)

### Example RPC

{% tabs %}
{% tab title="Curl" %}
<pre><code><strong>curl https://api.chainup.net/scroll/mainnet/&#x3C;YOUR_API_KEY> \
</strong>-X POST \
-H 'content-type: application/json' \
-H "CONSISTENT-HASH: true" \
---data '{"jsonrpc":"2.0","method":"getblock","params":[],"id":1}'  
</code></pre>
{% endtab %}

{% tab title="Javascript" %}
<pre class="language-javascript"><code class="lang-javascript"><strong>const axios = require('axios');
</strong>//npm install axios if you don have the module installed`
let options = {
    url: "https://api.chainup.net/scroll/mainnet/&#x3C;YOUR_API_KEY>",
    method: "post",
    headers:
    { 
     "content-type": "application/json"
    },
    body: JSON.stringify({"jsonrpc":"2.0","method":"getblock","params":[],"id":1})
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

headers = {"content-type": "application/json",
            "CONSISTENT-HASH": "true" }
payload = json.dumps({
    "id": 1,
    "jsonrpc": "2.0",
    "method": "getblock",
    "params": []
})
r = requests.post(url="https://api.chainup.net/scroll/mainnet/<YOUR_API_KEY>", headers=headers, data=payload)
if r.status_code == 200:
    print("Post successful: response: ", r.content)
else:
    print("An error has occurred: ", r.status_code)
```
{% endtab %}
{% endtabs %}

### Scroll Methods supported

* [`web3_clientVersion`](https://www.ankr.com/docs/rpc-service/chains/chains-api/scroll/#web3\_clientversion) — returns the current client version.
* [`web3_sha3`](https://www.ankr.com/docs/rpc-service/chains/chains-api/scroll/#web3\_sha3) — returns Keccak-256 (not the standardized SHA3-256) of the given data.
* [`net_version`](https://www.ankr.com/docs/rpc-service/chains/chains-api/scroll/#net\_version) — returns the current network ID.
* [`net_listening`](https://www.ankr.com/docs/rpc-service/chains/chains-api/scroll/#net\_listening) — returns true if client is actively listening for network connections.
* [`eth_syncing`](https://www.ankr.com/docs/rpc-service/chains/chains-api/scroll/#eth\_syncing) — returns data on the sync status or false.
* [`eth_gasPrice`](https://www.ankr.com/docs/rpc-service/chains/chains-api/scroll/#eth\_gasprice) — returns the current price per gas in wei.
* [`eth_accounts`](https://www.ankr.com/docs/rpc-service/chains/chains-api/scroll/#eth\_accounts) — returns a list of addresses owned by client.
* [`eth_blockNumber`](https://www.ankr.com/docs/rpc-service/chains/chains-api/scroll/#eth\_blocknumber) — returns the number of most recent block.
* [`eth_getBalance`](https://www.ankr.com/docs/rpc-service/chains/chains-api/scroll/#eth\_getbalance) — returns the balance of the account specified by address.
* [`eth_getStorageAt`](https://www.ankr.com/docs/rpc-service/chains/chains-api/scroll/#eth\_getstorageat) — returns the value from a storage position at an address specified.
* [`eth_getTransactionCount`](https://www.ankr.com/docs/rpc-service/chains/chains-api/scroll/#eth\_gettransactioncount) — returns the number of transactions sent from an address.
* [`eth_getBlockTransactionCountByHash`](https://www.ankr.com/docs/rpc-service/chains/chains-api/scroll/#eth\_getblocktransactioncountbyhash) — returns the number of transactions in a block specified by block hash.
* [`eth_getBlockTransactionCountByNumber`](https://www.ankr.com/docs/rpc-service/chains/chains-api/scroll/#eth\_getblocktransactioncountbynumber) — returns the number of transactions in the block specified by number.
* [`eth_getUncleCountByBlockHash`](https://www.ankr.com/docs/rpc-service/chains/chains-api/scroll/#eth\_getunclecountbyblockhash) — returns the number of uncles in a block specified by block hash.
* [`eth_getUncleCountByBlockNumber`](https://www.ankr.com/docs/rpc-service/chains/chains-api/scroll/#eth\_getunclecountbyblocknumber) — returns the number of uncles in a block specified by block number.
* [`eth_getCode`](https://www.ankr.com/docs/rpc-service/chains/chains-api/scroll/#eth\_getcode) — returns code at an address specified.
* [`eth_sendRawTransaction`](https://www.ankr.com/docs/rpc-service/chains/chains-api/scroll/#eth\_sendrawtransaction) — creates a new message call transaction or a contract creation for signed transactions.
* [`eth_call`](https://www.ankr.com/docs/rpc-service/chains/chains-api/scroll/#eth\_call) — executes a new message call immediately without creating a transaction on the blockchain.
* [`eth_estimateGas`](https://www.ankr.com/docs/rpc-service/chains/chains-api/scroll/#eth\_estimategas) — generates and returns an estimate of how much gas is necessary to allow the transaction to complete.
* [`eth_getBlockByHash`](https://www.ankr.com/docs/rpc-service/chains/chains-api/scroll/#eth\_getblockbyhash) — returns information for the block specified by block hash.
* [`eth_getBlockByNumber`](https://www.ankr.com/docs/rpc-service/chains/chains-api/scroll/#eth\_getblockbynumber) — returns information for the block specified by block number.
* [`eth_getTransactionByHash`](https://www.ankr.com/docs/rpc-service/chains/chains-api/scroll/#eth\_gettransactionbyhash) — returns information on a transaction specified by transaction hash.
* [`eth_getTransactionByBlockHashAndIndex`](https://www.ankr.com/docs/rpc-service/chains/chains-api/scroll/#eth\_gettransactionbyblockhashandindex) — returns information on a transaction specified by block hash and transaction index position.
* [`eth_getTransactionByBlockNumberAndIndex`](https://www.ankr.com/docs/rpc-service/chains/chains-api/scroll/#eth\_gettransactionbyblocknumberandindex) — returns information on a transaction by block number and transaction index position.
* [`eth_getTransactionReceipt`](https://www.ankr.com/docs/rpc-service/chains/chains-api/scroll/#eth\_gettransactionreceipt) — returns the receipt of a transaction by transaction hash.
* [`eth_getUncleByBlockHashAndIndex`](https://www.ankr.com/docs/rpc-service/chains/chains-api/scroll/#eth\_getunclebyblockhashandindex) — returns information about an uncle of a block by hash and uncle index position.
* [`eth_getUncleByBlockNumberAndIndex`](https://www.ankr.com/docs/rpc-service/chains/chains-api/scroll/#eth\_getunclebyblocknumberandindex) — returns information about an uncle of a block by number and uncle index position.
* [`eth_getLogs`](https://www.ankr.com/docs/rpc-service/chains/chains-api/scroll/#eth\_getlogs) — returns logs matching the parameters specified.
