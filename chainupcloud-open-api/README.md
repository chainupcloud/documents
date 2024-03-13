# ChainUpCloud Open API

## Base URL & Auth

[http://staking.chainup.net/${protocol}/${network}/${token}](http://staking.chainup.net/$%7Bprotocol%7D/$%7Bnetwork%7D/$%7Btoken%7D)

### **Support agreement**

| Agreement | Network |
| --------- | ------- |
| Ethereum  | Mainnet |

### **Path Params**

| **Parameter name** | **Data type** | **Whether it must be passed.** | **Description**                                                         |
| ------------------ | ------------- | ------------------------------ | ----------------------------------------------------------------------- |
| protocol           | string        | true                           | Protocol (ethereum)                                                     |
| token              | string        | true                           | Users are bound to Staking's token and authenticated through the token. |

\
**Create token**

1. ChainUp creates tokens and sends them to customers via email.
2. User side generates Token.

\
