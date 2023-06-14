# JSON-RPC methods

### Cosmos RPC

You can review the official **Dogecoin API documentation HERE.**&#x20;

### Example RPC

{% tabs %}
{% tab title="Curl" %}
<pre><code>curl https://api.chainup.net/dogecoin/mainnet/&#x3C;YOUR_API_KEY> \
-X POST \
<strong>-H 'content-type: application/json' \
</strong>--data '{"jsonrpc":"2.0","method":"/node_info","params":[],"id":1}' 
</code></pre>
{% endtab %}

{% tab title="Javascript" %}
```
    var Web3 = require('web3');
    var web3 = new Web3(new Web3.providers.HttpProvider());
    var version = web3.version.api;
            
    $.getJSON('https://api.arbiscan.io/api?module=contract&action=getabi&address=0x0000000000000000000000000000000000001004&apikey=YourApiKeyToken', function (data) {
    var contractABI = "";
        contractABI = JSON.parse(data.result);
        if (contractABI != ''){
            var MyContract = web3.eth.contract(contractABI);
            var myContractInstance = MyContract.at("0x0000000000000000000000000000000000001004");
            var result = myContractInstance.memberId("0xfe8ad7dd2f564a877cc23feea6c0a9cc2e783715");
            console.log("result1 : " + result);
            var result = myContractInstance.members(1);
            console.log("result2 : " + result);
        } else {
            console.log("Error" );
        }
    });
         
```
{% endtab %}

{% tab title="Python" %}
```
from web3 import Web3
import requests

# Connect to the Ethereum network
web3 = Web3(Web3.HTTPProvider('https://mainnet.infura.io/v3/your_infura_project_id'))

# Get the contract ABI from Arbiscan API
api_url = 'https://api.arbiscan.io/api'
api_params = {
    'module': 'contract',
    'action': 'getabi',
    'address': '0x0000000000000000000000000000000000001004',
    'apikey': 'YourApiKeyToken'
}
response = requests.get(api_url, params=api_params)
data = response.json()

if 'result' in data and data['result']:
    contractABI = data['result']
    myContract = web3.eth.contract(address='0x0000000000000000000000000000000000001004', abi=contractABI)
    
    result1 = myContract.functions.memberId('0xfe8ad7dd2f564a877cc23feea6c0a9cc2e783715').call()
    print("result1: " + str(result1))
    
    result2 = myContract.functions.members(1).call()
    print("result2: " + str(result2))
else:
    print("Error")

```
{% endtab %}
{% endtabs %}
