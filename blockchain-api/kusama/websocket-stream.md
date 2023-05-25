# WebSocket stream

Unlike HTTP, with WebSockets, you don't need to continuously make requests when you want specific information. WebSockets maintain a network connection for you (if done right) and listen for changes . You may view the official documentation [here](https://wiki.polkadot.network/docs/maintain-wss).&#x20;

{% tabs %}
{% tab title="WebSocket" %}
```
wscat -c wss://api.chainup.net/ws/kusama/mainnet/<YOUR_API_KEY>
<  {"jsonrpc":"2.0","method":"chain_getBlock","params":[],"id":32}
<  {"jsonrpc":"2.0","result":{"block":{"header":{"parentHash":"0x8a55738db2a55ee21eadf27756348c6e3883c93fc4c55424511da8c5ea8d3a13","number":"0xb04b2a", ... }
```
{% endtab %}

{% tab title="Javascript" %}
```
// Required imports
const { ApiPromise, WsProvider } = require('@polkadot/api');

async function main () {
  // Initialise the provider to connect to the local node
  const provider = new WsProvider('wss://api.chainup.net/ws/kusama/mainnet/<YOUR_API_KEY>');

  // Create the API and wait until ready
  const api = await ApiPromise.create({ provider });

  // Retrieve the chain & node information information via rpc calls
  const [chain, nodeName, nodeVersion] = await Promise.all([
    api.rpc.system.chain(),
    api.rpc.system.name(),
    api.rpc.system.version()
  ]);

  console.log(`You are connected to chain ${chain} using ${nodeName} v${nodeVersion}`);
}

main().catch(console.error).finally(() => process.exit());
```
{% endtab %}

{% tab title="Python" %}
```
import asyncio
from jsonrpc_websocket import Server

async def routine():
    server = Server('wss://api.chainup.net/ws/kusama/mainnet/<YOUR_API_KEY>')
    try:
        await server.ws_connect()

        chain = await server.api.rpc.system.chain()
        nodeName = await api.rpc.system.name()
        nodeVersion = await api.rpc.system.version()
        
        print(f'You are connected to chain {chain} using {nodeName} v{nodeVersion}')
    finally:
        await server.close()

asyncio.get_event_loop().run_until_complete(routine())
```
{% endtab %}
{% endtabs %}

