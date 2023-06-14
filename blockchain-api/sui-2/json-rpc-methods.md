# JSON-RPC methods

### Cosmos RPC

You can review the official [**Cosmos API documentation HERE.** ](https://docs.cosmos.network/swagger/)

### Example RPC

{% tabs %}
{% tab title="Curl" %}
<pre><code>curl https://api.chainup.net/cosmos/mainnet/&#x3C;YOUR_API_KEY> \
-X POST \
<strong>-H 'content-type: application/json' \
</strong>--data '{"jsonrpc":"2.0","method":"/node_info","params":[],"id":1}' 
</code></pre>
{% endtab %}

{% tab title="Javascript" %}
```
```
{% endtab %}

{% tab title="Python" %}
```
```
{% endtab %}
{% endtabs %}
