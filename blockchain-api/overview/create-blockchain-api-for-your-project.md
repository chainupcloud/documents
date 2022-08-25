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

GraphQL Endpoint

```
http://api.chainup.net/graphql/<PROTOCOL>/<NETWORK>/<TOKEN>
```

## Dedicated Node Endpoint

JSON-RPC Endpoint

```
http://<YOUR-NODE-ID>.blockchain.info/<TOKEN>
```

Websocket Endpoint

```
ws://<YOUR-NODE-ID>.blockchain.info/ws/<TOKEN>
```

GraphQL Endpoint

```
http://<YOUR-NODE-ID>.blockchain.info/graphql/<TOKEN>
```

## Using a project ID

Ethereum APIs require a valid project ID to be included with your request traffic. This identifier must be appended to the request URL. The following example shows how to do this for HTTPS or WebSocket requests:

{% tabs %}
{% tab title="HTTP" %}
```
curl http://api.chainup.net/ethereum/mainet/<TOKEN> \
    -X POST \
    -H "Content-Type: application/json" \
    -d '{"jsonrpc":"2.0","method":"eth_blockNumber","params":[],"id":1}'
```
{% endtab %}

{% tab title="WebSocket" %}
```
wscat -c ws://api.chainup.net/ws/ethereum/mainet/<TOKEN>
> {"jsonrpc":"2.0","method":"eth_blockNumber","params":[],"id":1}
```
{% endtab %}

{% tab title="GraphQL" %}
```
curl http://api.chainup.net/graphql/ethereum/mainet/<TOKEN> \
    -X POST \
    -H "Content-Type: application/json" \
    --data-raw '{"query":"{block(number: 123){hash transactionCount timestamp}}"}'
```
{% endtab %}
{% endtabs %}
