# Create Blockchain API for your project

## Blockchain API Endpoint

JSON-RPC Endpoint

```
http://api.chainup.net/<PROTOCOL>/<NETWORK>/<TOKEN>
```

Websocket Endpoint

```
ws://api.chainup.net/ws/<PROTOCOL>/<NETWORK>/<TOKEN>
```

## Using a token example&#x20;

Ethereum APIs require a valid project ID to be included with your request traffic. This identifier must be appended to the request URL. The following example shows how to do this for HTTPS or WebSocket requests:

{% tabs %}
{% tab title="HTTP" %}
```
curl http://api.chainup.net/ethereum/mainet/<TOKEN> \
    -X POST \
    -H "Content-Type: application/json" \
    -H "CONSISTENT-HASH: true" \
    -d '{"jsonrpc":"2.0","method":"eth_blockNumber","params":[],"id":1}'
```
{% endtab %}

{% tab title="WebSocket" %}
```
wscat -c ws://api.chainup.net/ws/ethereum/mainet/<TOKEN>
> {"jsonrpc":"2.0","method":"eth_blockNumber","params":[],"id":1}
```
{% endtab %}
{% endtabs %}

## Using a token example for Solana (Low latency domain)

When accessing solana you can use proprietary domain names to reduce network latency

{% tabs %}
{% tab title="HTTP" %}
```
curl http://sol.chainup.net/<TOKEN> \
    -X POST \
    -H "Content-Type: application/json" \
    -d '{"jsonrpc":"2.0","id":1, "method":"getSlot"}'
```
{% endtab %}

{% tab title="WebSocket" %}
```
wscat -c ws://sol.chainup.net/ws/<TOKEN>
> { "jsonrpc": "2.0", "id": 1, "method": "slotSubscribe"}
```
{% endtab %}
{% endtabs %}

## Supported protocols

<table><thead><tr><th width="131.0859375">PROTOCOL</th><th width="265.8828125">NETWORK</th><th width="138">Schema</th><th>domain</th></tr></thead><tbody><tr><td>ethereum</td><td>mainnet,goerli,holesky,sepolia</td><td>https,wss</td><td>api.chainup.net (default)</td></tr><tr><td>solana</td><td>mainnet</td><td>https,wss</td><td><strong>sol.chainup.net</strong> </td></tr><tr><td>ton</td><td>mainnet</td><td>https</td><td>api.chainup.net</td></tr><tr><td>bsc</td><td>mainnet,testnet</td><td>https,wss</td><td>api.chainup.net</td></tr><tr><td>polygon</td><td>mainnet,mumbai</td><td>https,wss</td><td>api.chainup.net</td></tr><tr><td>tron</td><td>mainnet</td><td>https</td><td>api.chainup.net</td></tr><tr><td>ethereum2</td><td>mainnet,prater,holesky,sepolia</td><td>https</td><td>api.chainup.net</td></tr><tr><td>polkadot</td><td>mainnet,westend</td><td>https,wss</td><td>api.chainup.net</td></tr><tr><td>filecoin</td><td>mainnet,calibration,hyperspace</td><td>https</td><td>api.chainup.net</td></tr><tr><td>ipfs</td><td>pub</td><td>https</td><td>api.chainup.net</td></tr><tr><td>bitcoin</td><td>mainnet,testnet,testnet4,signet</td><td>https</td><td>api.chainup.net</td></tr><tr><td>litecoin</td><td>mainnet,testnet</td><td>https</td><td>api.chainup.net</td></tr><tr><td>near</td><td>mainnet,testnet</td><td>https</td><td>api.chainup.net</td></tr><tr><td>etc</td><td>mainnet</td><td>https,wss</td><td>api.chainup.net</td></tr><tr><td>bch</td><td>mainnet</td><td>https</td><td>api.chainup.net</td></tr><tr><td>kusama</td><td>mainnet</td><td>https,wss</td><td>api.chainup.net</td></tr><tr><td>bsv</td><td>mainnet</td><td>https</td><td>api.chainup.net</td></tr><tr><td>eos</td><td>mainnet</td><td>https</td><td>api.chainup.net</td></tr><tr><td>fantom</td><td>mainnet</td><td>https,wss</td><td>api.chainup.net</td></tr><tr><td>aptos</td><td>mainnet</td><td>https</td><td>api.chainup.net</td></tr><tr><td>sui</td><td>mainnet,testnet</td><td>https,wss</td><td>api.chainup.net</td></tr><tr><td>avax</td><td>mainnet</td><td>https,wss</td><td>api.chainup.net</td></tr><tr><td>arbitrum</td><td>mainnet</td><td>https,wss</td><td>api.chainup.net</td></tr><tr><td>omni</td><td>mainnet</td><td>https</td><td>api.chainup.net</td></tr><tr><td>cosmos</td><td>mainnet</td><td>https</td><td>api.chainup.net</td></tr><tr><td>dogecoin</td><td>mainnet</td><td>https,wss</td><td>api.chainup.net</td></tr><tr><td>optimism</td><td>mainnet,goerli</td><td>https,wss</td><td>api.chainup.net</td></tr><tr><td>xrp</td><td>mainnet</td><td>https,wss</td><td>api.chainup.net</td></tr><tr><td>dash</td><td>mainnet</td><td>https</td><td>api.chainup.net</td></tr><tr><td>zcash</td><td>mainnet</td><td>https</td><td>api.chainup.net</td></tr><tr><td>base</td><td>mainnet</td><td>https,wss</td><td>api.chainup.net</td></tr><tr><td>scroll</td><td>mainnet</td><td>https,wss</td><td>api.chainup.net</td></tr><tr><td>qtum</td><td>mainnet</td><td>https</td><td>api.chainup.net</td></tr><tr><td>starknet</td><td>mainnet</td><td>https</td><td>api.chainup.net</td></tr><tr><td>blast</td><td>mainnet</td><td>https,wss</td><td>api.chainup.net</td></tr><tr><td>worldchain</td><td>mainnet</td><td>https</td><td>api.chainup.net</td></tr></tbody></table>
