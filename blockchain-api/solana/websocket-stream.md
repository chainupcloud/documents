# Websocket Stream

Unlike HTTP, with WebSockets, you don't need to continuously make requests when you want specific information. WebSockets maintain a network connection for you (if done right) and listen for changes . You may view the[ **official Solana Websocket documentation here.** ](https://solana.com/docs/rpc/websocket)

{% tabs %}
{% tab title="WebSocket" %}
<pre><code>wscat -c wss://api.chainup.net/ws/solana/mainnet/&#x3C;YOUR_API_KEY>
<strong>
</strong><strong>&#x3C; {"jsonrpc": "2.0", "id": 0, "method": "accountUnsubscribe", "params": [0]}
</strong>&#x3C;  { "jsonrpc": "2.0", "result": true, "id": 1 }
</code></pre>
{% endtab %}

{% tab title="Javascript" %}
<pre><code><strong>const Web3 = require('web3');
</strong>
const web3 = new Web3("wss://api.chainup.net/ws/solana/mainnet/&#x3C;YOUR_API_KEY>")

web3.solana.getBlockSlot().then(console.log) // -> 1022457

</code></pre>
{% endtab %}

{% tab title="Python" %}
```
from web3 import Web3

websocket_url='wss://api.chainup.net/ws/solana/mainnet/<YOUR_API_KEY>'
w3 = Web3(Web3.WebsocketProvider(websocket_url))

# You can check if the connection is established using isConnected function.
w3.isConnected()

# Output: True
```
{% endtab %}
{% endtabs %}
