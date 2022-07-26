# WebSocket stream

Unlike HTTP, with WebSockets, you don't need to continuously make requests when you want specific information. WebSockets maintain a network connection for you (if done right) and listen for changes . You may view the official documentation [here](https://ethereum.org/ml/developers/tutorials/using-websockets/).&#x20;

{% tabs %}
{% tab title="WebSocket" %}
```
wscat -c wss://api.chainup.net/ws/ethereum/mainnet/58c9400ca6f04d7c8269c7843738aedd
<  {"jsonrpc":  "2.0", "id": 0, "method":  "eth_gasPrice"}
<  {"jsonrpc":"2.0","id":0,"result":"0x6f56b59ac"}
```
{% endtab %}
{% endtabs %}

``
