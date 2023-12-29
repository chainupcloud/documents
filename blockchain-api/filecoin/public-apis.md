---
description: >-
  The Public API has minimum service rates, making it suitable for use with
  MetaMask. To access premium support, register with ChainUp Cloud
---

# Public APIs

{% hint style="info" %}
Note That each ip address is limited to only 60 request per minute.
{% endhint %}

### Endpoints

[https://filecoin.chainup.net/rpc/v1\
https://filecoin-calibration.chainup.net/rpc/v1\
https://filecoin-hyperspace.chainup.net/rpc/v1](https://filecoin.chainup.net/rpc/v1https://filecoin-calibration.chainup.net/rpc/v1https://filecoin-hyperspace.chainup.net/rpc/v1)

{% hint style="info" %}
We only collect user IP addresses for the purpose of rate limiting. For more information, please visit: [https://www.chainup.com/privacyPolicy](https://www.chainup.com/privacyPolicy)
{% endhint %}

### **Available Filecoin API request methods**

```
      Filecoin.ChainGetBlockMessages
      Filecoin.ChainGetGenesis
      Filecoin.ChainGetMessage
      Filecoin.ChainGetParentMessages
      Filecoin.ChainGetParentReceipts
      Filecoin.ChainGetPath
      Filecoin.ChainGetTipSet
      Filecoin.ChainGetTipSetAfterHeight
      Filecoin.ChainGetTipSetByHeight
      Filecoin.ChainHasObj
      Filecoin.ChainHead
      Filecoin.ChainPutObj
      Filecoin.ChainReadObj
      Filecoin.Discover
      Filecoin.EthAccounts
      Filecoin.EthBlockNumber
      Filecoin.EthCall
      Filecoin.EthChainId
      Filecoin.EthEstimateGas
      Filecoin.EthFeeHistory
      Filecoin.EthGasPrice
      Filecoin.EthGetBalance
      Filecoin.EthGetBlockByHash
      Filecoin.EthGetBlockByNumber
      Filecoin.EthGetBlockTransactionCountByHash
      Filecoin.EthGetBlockTransactionCountByNumber
      Filecoin.EthGetCode
      Filecoin.EthGetFilterChanges
      Filecoin.EthGetFilterLogs
      Filecoin.EthGetLogs
      Filecoin.EthGetMessageCidByTransactionHash
      Filecoin.EthGetStorageAt
      Filecoin.EthGetTransactionByHash
      Filecoin.EthGetTransactionCount
      Filecoin.EthGetTransactionHashByCid
      Filecoin.EthGetTransactionReceipt
      Filecoin.EthMaxPriorityFeePerGas
      Filecoin.EthNewBlockFilter
      Filecoin.EthNewFilter
      Filecoin.EthNewPendingTransactionFilter
      Filecoin.EthProtocolVersion
      Filecoin.EthSendRawTransaction
      Filecoin.EthSubscribe
      Filecoin.EthUninstallFilter
      Filecoin.EthUnsubscribe
      Filecoin.GasEstimateGasPremium
      Filecoin.GasEstimateMessageGas
      Filecoin.MpoolGetNonce
      Filecoin.MpoolPush
      Filecoin.MsigGetAvailableBalance
      Filecoin.MsigGetPending
      Filecoin.MsigGetVested
      Filecoin.MsigGetVestingSchedule
      Filecoin.NetListening
      Filecoin.NetVersion
      Filecoin.StateAccountKey
      Filecoin.StateCall
      Filecoin.StateDealProviderCollateralBounds
      Filecoin.StateDecodeParams
      Filecoin.StateGetActor
      Filecoin.StateListMiners
      Filecoin.StateLookupID
      Filecoin.StateMarketBalance
      Filecoin.StateMarketStorageDeal
      Filecoin.StateMinerInfo
      Filecoin.StateMinerPower
      Filecoin.StateMinerProvingDeadline
      Filecoin.StateMinerSectorCount
      Filecoin.StateNetworkName
      Filecoin.StateNetworkVersion
      Filecoin.StateReadState
      Filecoin.StateReplay
      Filecoin.StateSearchMsg
      Filecoin.StateSectorGetInfo
      Filecoin.StateVerifiedClientStatus
      Filecoin.StateVerifierStatus
      Filecoin.StateWaitMsg
      Filecoin.Version
      Filecoin.WalletBalance
      Filecoin.Web3ClientVersion
```
