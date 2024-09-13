---
description: >-
  Welcome to the  Chainup TON API documentation! This resource provides
  essential information for developers looking to integrate with the TON
  blockchain.
icon: icons
---

# TON

## Overview of TON APIs

### TON offers two primary services for accessing blockchain data:

1. **TON HTTP API**: This API converts the ADNL binary protocol to HTTP, allowing you to communicate with TON nodes as if you were directly connected. It's designed for ease of use and compatibility with standard web technologies.
2. **TON Indexer API**: This service indexes blockchain data into PostgreSQL, enabling efficient data retrieval through API calls. It is particularly useful for applications that require access to historical blockchain data.

## Accessing the APIs

* **TON HTTP API Base URL**:\
  `https://api.chainup.net/ton/mainnet/{token}/api/v2`
* **TON Indexer API Base URL**:\
  `https://api.chainup.net/ton/mainnet/{token}/api/v3`

## Example Usage

You can interact with the APIs using standard HTTP requests. Below are examples of how to fetch masterchain information:

## Using the TON HTTP API

```
curl -X 'GET' \
  'https://api.chainup.net/ton/mainnet/{token}/api/v2/getMasterchainInfo' \
  -H 'accept: application/json'
```

## Using the TON Indexer API

```
curl -X 'GET' \
  'https://api.chainup.net/ton/mainnet/{token}/api/v3/masterchainInfo' \
  -H 'accept: application/json'
```

### Note on ADNL Protocol

TON nodes do not provide HTTP RPC APIs and communicate exclusively through the ADNL binary protocol. If you require access methods for ADNL, please reach out to our support team for assistance.

