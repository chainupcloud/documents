# JSON-RPC methods

##



| Methods          | Supported         |
| ---------------- | ----------------- |
| JSON-RPC 2.0     |                 ✅ |
| WebSocket stream |                 ✅ |
| GraphQL          |                 ✅ |
|                  |                   |



| Types of Requests                               | Supported        |
| ----------------------------------------------- | ---------------- |
| [Block Info](./#getting-blocks)                 |                ✅ |
| [Reading Transactions](./#reading-transactions) |               ✅  |
| [Account Information](./#account-information)   |               ✅  |
| [Event Logs](./#event-logs)                     |               ✅  |
| [Chain Information](./#chain-information)       |               ✅  |
| [Getting Uncles](./#getting-uncles)             |               ✅  |
| [Web3](./#web3)                                 |               ✅  |





### Getting Blocks&#x20;

Fetches information from a certain block in the blockchain.

* [eth\_blockNumber](./#eth\_blocknumber)
* [eth\_getBlockByHash](./#eth\_getblockbyhash)
* [eth\_getBlockByNumber](./#eth\_getblockbynumber)

#### eth\_blockNumber

{% tabs %}
{% tab title="Curl" %}
```
curl  https://api.chainup.net/ethereum/mainnet/<YOUR_API_KEY> \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_blockNumber","params":[],"id":0}'
```
{% endtab %}
{% endtabs %}

#### eth\_getBlockByHash

{% tabs %}
{% tab title="Curl" %}
```
curl  https://api.chainup.net/ethereum/mainnet/<YOUR_API_KEY>  \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_getBlockByHash","params":["0xc0f4906fea23cf6f3cce98cb44e8e1449e455b28d684dfa9ff65426495584de6", true],"id":0}'
```
{% endtab %}
{% endtabs %}

#### eth\_getBlockByNumber

{% tabs %}
{% tab title="Curl" %}
```
curl  https://api.chainup.net/ethereum/mainnet/<YOUR_API_KEY>  \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_getBlockByNumber","params":["0x1b4", true],"id":0}'
```
{% endtab %}
{% endtabs %}



### Reading Transactions

Fetches information on the state data for addresses regardless of whether it is a user or a smart contract.

* [eth\_getTransactionByHash](./#eth\_gettransactionbyhash)
* [eth\_getTransactionCount](./#eth\_gettransactioncount)
* [eth\_getTransactionReceipt](./#eth\_gettransactionreceipt)
* [eth\_getBlockTransactionCountByHash](./#eth\_getblocktransactioncountbyhash)
* [eth\_getBlockTransactionCountByNumber](./#eth\_getblocktransactioncountbynumber)
* [eth\_getTransactionByBlockHashAndIndex](./#eth\_gettransactionbyblockhashandindex)
* [eth\_getTransactionByBlockNumberAndIndex](./#eth\_gettransactionbyblocknumberandindex)



#### eth\_getTransactionByHash

{% tabs %}
{% tab title="Curl" %}
```
curl  https://api.chainup.net/ethereum/mainnet/58c9400ca6f04d7c8269c7843738aedd  \
-X POST \
-H "Content-Type: application/json" \
-d'{"jsonrpc":"2.0","method":"eth_getTransactionByHash","params":["0x88df016429689c079f3b2f6ad39fa052532c56795b733da78a91ebe6a713944b"],"id":0}'
```
{% endtab %}
{% endtabs %}

#### eth\_getTransactionCount

{% tabs %}
{% tab title="Curl" %}
```
curl  https://api.chainup.net/ethereum/mainnet/<YOUR_API_KEY>  \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_getTransactionCount","params":["0xc94770007dda54cF92009BFF0dE90c06F603a09f","latest"],"id":0}'
```
{% endtab %}
{% endtabs %}

#### eth\_getTransactionReceipt

{% tabs %}
{% tab title="Curl" %}
```
curl  https://api.chainup.net/ethereum/mainnet/<YOUR_API_KEY> \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_getTransactionReceipt","params":["0xab059a62e22e230fe0f56d8555340a29b2e9532360368f810595453f6fdd213b"],"id":0}
```
{% endtab %}
{% endtabs %}

#### eth\_getBlockTransactionCountByHash

{% tabs %}
{% tab title="Curl" %}
```
curl  [https://api.chainup.net/ethereum/mainnet/<YOUR_API_KEY>](https://api.chainup.net/ethereum/mainnet/58c9400ca6f04d7c8269c7843738aedd)   \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_getBlockTransactionCountByHash","params":["0x8243343df08b9751f5ca0c5f8c9c0460d8a9b6351066fae0acbd4d3e776de8bb"],"id":0}'
```
{% endtab %}
{% endtabs %}

#### eth\_getBlockTransactionCountByNumber

{% tabs %}
{% tab title="Curl" %}
```
curl https://api.chainup.net/ethereum/mainnet/<YOUR_API_KEY>   \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_getBlockTransactionCountByNumber","params":["latest"],"id":0}'
```
{% endtab %}
{% endtabs %}

#### eth\_getTransactionByBlockHashAndIndex

{% tabs %}
{% tab title="Curl" %}
```
curl  https://api.chainup.net/ethereum/mainnet/<YOUR_API_KEY>    \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_getTransactionByBlockHashAndIndex","params":["0xc0f4906fea23cf6f3cce98cb44e8e1449e455b28d684dfa9ff65426495584de6", "0x0"],"id":0}'
```
{% endtab %}
{% endtabs %}

#### eth\_getTransactionByBlockNumberAndIndex

{% tabs %}
{% tab title="Curl" %}
```
curl  https://api.chainup.net/ethereum/mainnet/<YOUR_API_KEY>    \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_getTransactionByBlockNumberAndIndex","params":["latest", "0x0"],"id":0}'
```
{% endtab %}
{% endtabs %}



### Account Information

Returns information regarding an address's stored on-chain data.

* [eth\_getBalance](./#eth\_getbalance)
* [eth\_getStorageAt](./#eth\_getstorageat)
* [eth\_getCode](./#eth\_getcode)
* [eth\_accounts](./#eth\_accounts)
* [eth\_getProof](./#eth\_getproof)



#### eth\_getBalance

{% tabs %}
{% tab title="Curl" %}
```
curl   https://api.chainup.net/ethereum/mainnet/<YOUR_API_KEY>   \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_getBalance","params":["0xc94770007dda54cF92009BFF0dE90c06F603a09f", "latest"],"id":0}'
```
{% endtab %}
{% endtabs %}

#### eth\_getStorageAt

{% tabs %}
{% tab title="Curl" %}
```
curl  https://api.chainup.net/ethereum/mainnet/<YOUR_API_KEY>    \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0", "method": "eth_getStorageAt", "params": ["0x295a70b2de5e3953354a6a8344e616ed314d7251", "0x0", "latest"], "id": 1}'
```
{% endtab %}
{% endtabs %}

#### eth\_getCode

{% tabs %}
{% tab title="Curl" %}
```
curl  https://api.chainup.net/ethereum/mainnet/<YOUR_API_KEY>   \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_getCode","params":["0xb59f67a8bff5d8cd03f6ac17265c550ed8f33907", "latest"],"id":0}'
```
{% endtab %}
{% endtabs %}

#### eth\_accounts

{% tabs %}
{% tab title="Curl" %}
```
curl https://api.chainup.net/ethereum/mainnet/<YOUR_API_KEY>  \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_accounts","params":[],"id":1}'
```
{% endtab %}
{% endtabs %}

#### eth\_getProof

{% tabs %}
{% tab title="Curl" %}
```
curl  https://api.chainup.net/ethereum/mainnet/58c9400ca6f04d7c8269c7843738aedd   \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_getProof","params":["0x7F0d15C7FAae65896648C8273B6d7E43f58Fa842",["0x56e81f171bcc55a6ff8345e692c0f86e5b48e01b996cadc001622fb5e363b421"],"latest"],"id":1}'
```
{% endtab %}
{% endtabs %}





### Event Logs

Returns logs which are records that denote/provide context on specific events within a smart contract, like a token transfer or a change of ownership for example.

* [eth\_getLogs](./#eth\_getlogs)
* [eth\_newBlockFilter](./#eth\_newblockfilter)
* [eth\_newFilter](./#eth\_newfilter)
* [eth\_newPendingTransactionFilter](./#eth\_newpendingtransactionfilter)
* [eth\_uninstallFilter ](./#eth\_uninstallfilter)



#### eth\_getLogs

{% tabs %}
{% tab title="Curl" %}
```
curl  https://api.chainup.net/ethereum/mainnet/<YOUR_API_KEY> \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_getLogs","params":[{"address": "0xb59f67a8bff5d8cd03f6ac17265c550ed8f33907","topics": ["0xddf252ad1be2c89b69c2b068fc378daa952ba7f163c4a11628f55a4df523b3ef"],"blockHash": "0x8243343df08b9751f5ca0c5f8c9c0460d8a9b6351066fae0acbd4d3e776de8bb"}],"id":0}'
```
{% endtab %}
{% endtabs %}

#### eth\_newBlockFilter

{% tabs %}
{% tab title="Curl" %}
```
curl https://api.chainup.net/ethereum/mainnet/<YOUR_API_KEY>  \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_newBlockFilter","params":[],"id":0}'
```
{% endtab %}
{% endtabs %}

#### eth\_newFilter

{% tabs %}
{% tab title="Curl" %}
```
curl
https://eth-mainnet.alchemyapi.io/v2/your-api-key \
-X POST \
-H "Content-Type: application/json" \ 
-d '{"jsonrpc":"2.0","method":"eth_newFilter","params":[{"fromBlock": "0x1","toBlock": "0x2","address": "0x8888f1f195afa192cfee860698584c030f4c9db1","topics": ["0x000000000000000000000000a94f5374fce5edbc8e2a8697c15331677e6ebf0b", null, ["0x000000000000000000000000a94f5374fce5edbc8e2a8697c15331677e6ebf0b", "0x0000000000000000000000000aff3454fce5edbc8cca8697c15331677e6ebccc"]]}],"id":0}'

```
{% endtab %}
{% endtabs %}



#### eth\_newPendingTransactionFilter

{% tabs %}
{% tab title="Curl" %}
```
curl https://api.chainup.net/ethereum/mainnet/<YOUR_API_KEY> \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_newPendingTransactionFilter","params":[],"id":0}'
```
{% endtab %}
{% endtabs %}

#### eth\_uninstallFilter

{% tabs %}
{% tab title="Curl" %}
```
curl https://eth-mainnet.alchemyapi.io/v2/your-api-key \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_uninstallFilter","params":["0xfe704947a3cd3ca12541458a4321c869"],"id":0}'
```
{% endtab %}
{% endtabs %}



### Chain Information

Returns information on the Ethereum network and internal settings.

* [eth\_gasPrice](./#eth\_gasprice)
* [eth\_estimateGas](./#eth\_estimategas)
* [eth\_feeHistory](./#eth\_feehistory)
* [eth\_maxPriorityFeePerGas](./#eth\_maxpriorityfeepergas)
* [eth\_chainId](./#eth\_chainid)
* [net\_version](./#net\_version)
* [net\_listening](./#net\_listening)



#### eth\_gasPrice

{% tabs %}
{% tab title="Curl" %}
```
curl https://api.chainup.net/ethereum/mainnet/<YOUR_API_KEY> \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_gasPrice","params":[],"id":0}'
```
{% endtab %}
{% endtabs %}

#### eth\_estimateGas

{% tabs %}
{% tab title="Curl" %}
```
curl https://api.chainup.net/ethereum/mainnet/<YOUR_API_KEY>  \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_estimateGas","params":[{"from": "0x8D97689C9818892B700e27F316cc3E41e17fBeb9","to": "0xd3CdA913deB6f67967B99D67aCDFa1712C293601","value": "0x186a0"}],"id":1}'
```
{% endtab %}
{% endtabs %}

#### eth\_feeHistory

{% tabs %}
{% tab title="Curl" %}
```
curl https://api.chainup.net/ethereum/mainnet/<YOUR_API_KEY>  \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_feeHistory","params":[4, "latest", [25, 75]],"id":1}'
```
{% endtab %}
{% endtabs %}

#### eth\_maxPriorityFeePerGas

{% tabs %}
{% tab title="Curl" %}
```
curl https://api.chainup.net/ethereum/mainnet/<YOUR_API_KEY>  \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_maxPriorityFeePerGas","params":[],"id":1}'
```
{% endtab %}
{% endtabs %}

#### `eth_chainId`

{% tabs %}
{% tab title="Curl" %}
```
curl https://api.chainup.net/ethereum/mainnet/<YOUR_API_KEY>  \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_chainId","params":[],"id":83}'
```
{% endtab %}
{% endtabs %}

#### `net_version`

{% tabs %}
{% tab title="Curl" %}
```
curl https://api.chainup.net/ethereum/mainnet/<YOUR_API_KEY>  \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"net_version","params":[],"id":67}'
```
{% endtab %}
{% endtabs %}

#### net\_listening

{% tabs %}
{% tab title="Curl" %}
```
curl https://api.chainup.net/ethereum/mainnet/<YOUR_API_KEY>  \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"net_listening","params":[],"id":67}'
```
{% endtab %}
{% endtabs %}



### Getting Uncles

Returns information on uncle blocks are which are network rejected blocks and replaced by a canonical block instead.

[eth\_getUncleByBlockHashAndIndex](./#eth\_getunclebyblockhashandindex)

[eth\_getUncleByBlockNumberAndIndex](./#eth\_getunclebyblocknumberandindex)

[eth\_getUncleCountByBlockHash](./#eth\_getunclecountbyblockhash)

[eth\_getUncleCountByBlockNumber](./#eth\_getunclecountbyblocknumber)



#### eth\_getUncleByBlockHashAndIndex

{% tabs %}
{% tab title="Curl" %}
```
curl https://api.chainup.net/ethereum/mainnet/<YOUR_API_KEY> \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_getUncleByBlockHashAndIndex","params":["0xb3b20624f8f0f86eb50dd04688409e5cea4bd02d700bf6e79e9384d47d6a5a35", "0x0"],"id":0}'
```
{% endtab %}
{% endtabs %}

#### `eth_getUncleByBlockNumberAndIndex`

{% tabs %}
{% tab title="Curl" %}
```
curl https://api.chainup.net/ethereum/mainnet/<YOUR_API_KEY>  \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_getUncleByBlockNumberAndIndex","params":["0x29c", "0x0"],"id":0}'
```
{% endtab %}
{% endtabs %}

#### `eth_getUncleCountByBlockHash`

{% tabs %}
{% tab title="Curl" %}
```
curl https://api.chainup.net/ethereum/mainnet/<YOUR_API_KEY> \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_getUncleCountByBlockHash","params":["0xb3b20624f8f0f86eb50dd04688409e5cea4bd02d700bf6e79e9384d47d6a5a35"],"id":0}'
```
{% endtab %}
{% endtabs %}

#### eth\_getUncleCountByBlockNumber

{% tabs %}
{% tab title="Curl" %}
```
curl https://api.chainup.net/ethereum/mainnet/<YOUR_API_KEY> \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"eth_getUncleCountByBlockNumber","params":["0xe8"],"id":1}'
```
{% endtab %}
{% endtabs %}

### Web3

Returns Ethereum network configuration information.

****[**web3\_clientVersion**](./#web3\_clientversion)****

****[**web3\_sha3**](./#web3\_sha3)****

****

#### web3\_clientVersion

{% tabs %}
{% tab title="Curl" %}
```
curl https://api.chainup.net/ethereum/mainnet/<YOUR_API_KEY>  \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"web3_clientVersion","params":[],"id":0}'
```
{% endtab %}
{% endtabs %}

#### `web3_sha3`

{% tabs %}
{% tab title="Curl" %}
```
curl https://api.chainup.net/ethereum/mainnet/<YOUR_API_KEY> \
-X POST \
-H "Content-Type: application/json" \
-d '{"jsonrpc":"2.0","method":"web3_sha3","params":["0x68656c6c6f20776f726c64"],"id":64}'
```
{% endtab %}
{% endtabs %}



