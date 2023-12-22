# WebSocket stream

Unlike HTTP, with WebSockets, you don't need to continuously make requests when you want specific information. WebSockets maintain a network connection for you (if done right) and listen for changes . You may view the official documentation [here](https://ethereum.org/ml/developers/tutorials/using-websockets/).&#x20;

{% tabs %}
{% tab title="WebSocket" %}
```
wscat -c wss://api.chainup.net/ws/ethereum/mainnet/<YOUR_API_KEY>
<  {"jsonrpc":  "2.0", "id": 0, "method":  "eth_gasPrice"}
<  {"jsonrpc": "2.0","id":0,"result":"0x6f56b59ac"}
```
{% endtab %}

{% tab title="Javascript" %}
<pre><code><strong>const Web3 = require('web3');
</strong>
const web3 = new Web3("wss://api.chainup.net/ws/ethereum/mainnet/&#x3C;YOUR_API_KEY>")

web3.eth.getBlockNumber().then(console.log) // -> 9022457

</code></pre>
{% endtab %}

{% tab title="Python" %}
```
from web3 import Web3

websocket_url='wss://api.chainup.net/ws/ethereum/mainnet/<YOUR_API_KEY>'
w3 = Web3(Web3.HTTPProvider(websocket_url))

# You can check if the connection is established using isConnected function.
w3.isConnected()

# Output: True
```
{% endtab %}
{% endtabs %}

