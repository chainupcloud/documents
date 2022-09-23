# 📀 Shanghai Upgrade

### 1.    EVM Object Format ⚙️

The [EIP-3540](https://eips.ethereum.org/EIPS/eip-3540) proposal looks to separate code and data with the creation of an Ethereum Virtual Machine (EVM) Object Format , the proposed solution for on-chain code validation : provide new functionality to contracts which are deployed with a specific identifier, but leave existing contracts executing as is. &#x20;

This could also pave the way toward introducing new contract code sections types that could help enable currently complicated features, such as [Account Abstraction](https://eips.ethereum.org/EIPS/eip-4337), [control flow in the EVM](https://eips.ethereum.org/EIPS/eip-4200) and [EIP-3074](https://eips.ethereum.org/EIPS/eip-3074). A companion EIP to 3540, [EIP-3670](https://eips.ethereum.org/EIPS/eip-3670) will enable code validation for (EVM Object Format) contracts upon deployment.

### &#x20;2.    Beacon Chain Withdrawals 🏧

Another major feature for Shanghai is the activation of Beacon Chain withdrawals:  [EIP-4895: Beacon chain push withdrawals as operations](https://eips.ethereum.org/EIPS/eip-4895) , which unlocks the Ether locked up, pre-merge phase.

A [meta-spec](https://notes.ethereum.org/@ralexstokes/Skp1mPSb9) outlines how the entire process works. At a high level, in each slot, the Beacon Chain can process a set number of full or partial withdrawals. These withdrawals are tracked in receipts which contain the amount, destination address and unique index of each withdrawal. As part of the block creation and validation process, these withdrawals are then credited on the execution layer, similarly to how proof-of-work issuance is credited to miners today.

In short, even after the Shanghai Upgrade, it is possible to withdraw, subsequently in a queue manner, as there is a limit of validators that can enter and leave the network, for security reasons, in case of a malicious attack, this will buy time for detection and slashing of the attacker’s funds.

### 3.    Layer 2 Fee Reductions 📉

The Ethereum core team hope to include in Shanghai is a reduction of fees on layer 2. Because L2s post their transaction data (and/or proofs) on L1, a large part of end users' transaction fees come from the amortized gas costs of L1 data storage. Sharding offers a cheaper alternative for L2s to post their data, but while the specification seems to have settled, a full sharding implementation isn't ready yet.

In the meantime, two options are available to reduce these costs: either a `CALLDATA` cost reduction on mainnet, or a "proto-sharding" implementation, possible with the introduction of a new transaction type on Ethereum, called Shard Blob Transactions.

#### **`CALLDATA` Cost Reduction**

As the full-sharding implementation isn’t ready yet, the platform plans to reduce transaction fees on L2 by lowering the cost of data on layer 1 (L1). This EIP helps to balance out the increasing block sizes. It proposes a maximum cap to the amount of CALLDATA in a block. It is a simple change with significant fee reductions on Layer 2.

The simplest way to reduce transaction fees on L2s is to lower the cost of storing data on L1. [EIP-4488](https://eips.ethereum.org/EIPS/eip-4488) proposes to do this, reducing the cost from 16 gas per byte of `CALLDATA` to 3 gas/byte. This reduced storage cost would translate to lower L2 fees.

#### **Shard Blob Transactions**

Another proposal, which gets us closer to a full sharding deployment, is [EIP-4844](https://eips.ethereum.org/EIPS/eip-4844) , which introduces Shard Blob Transactions. At a high-level, this new type of transaction would include commitments to blobs of data which are gossiped on the Beacon Chain.

&#x20;This proposal can be thought of as a "mini-sharding", where instead of relying on data availability sampling, every node on the network needs to validate all the data in blobs. The key point is that data inside the blobs can be be stored on secondary blockchains after a period of time and only made accessible only when needed, so it won’t increase the main blockchain size considerably.

### 4. References

Shanghai Upgrade Specs - [https://github.com/ethereum/execution...](https://www.youtube.com/redirect?event=video\_description\&redir\_token=QUFFLUhqa2JNdzBLbDBZZjVjdGN6UjJERTc1LWdaUU1GUXxBQ3Jtc0ttUF9idi1BNjFZSnh3UTY4bUNUU2dvSDFmNmlLYnBfRXNsNGhMS1MzZ0dJUUVIZVFUWW8wRnRWaHdiUWVnbmo2WmlFVUlUQ04yRnhuLVltTUJVM1JmTTk0QWQwNUhFUTBlQk5qQ3BleC00MUo3RHprcw\&q=https%3A%2F%2Fgithub.com%2Fethereum%2Fexecution-specs%2Fblob%2Fmaster%2Fnetwork-upgrades%2Fmainnet-upgrades%2Fshanghai.md\&v=65hxeeox1iI)

EIP-3540: Implementation of EVM Object Format (EOF) - https://eips.ethereum.org/EIPS/eip-3540

Beacon Chain Withdrawals - [https://eips.ethereum.org/EIPS/eip-4895](https://www.youtube.com/redirect?event=video\_description\&redir\_token=QUFFLUhqbW5ZV09jZW9TREpDZmFkcW91ZWItOFVfblJWQXxBQ3Jtc0ttOENMT1dVYldVaGZwMk10Q3pDWHJlbkx1Nm94b1llekVtODVlYU9jb3pTWVU1dG9mNlNEQkdtQlFDYTRPUDVNdFNfdGJKUnFYeVVtY0d3eGV3dWd0aHJWUnF4WjZTYVF3SEcwcDVOSFEweHd1MDQ2NA\&q=https%3A%2F%2Feips.ethereum.org%2FEIPS%2Feip-4895\&v=65hxeeox1iI)

&#x20;Fee Reductions - [https://eips.ethereum.org/EIPS/eip-4488](https://www.youtube.com/redirect?event=video\_description\&redir\_token=QUFFLUhqbUZsUGczN2xXalEwbXhocjZQMlY4NTV3MDdEUXxBQ3Jtc0tsclBUQWJoRGZzTm5PVXZYcXE1VThkekJwc0dxUEZrUjY4QnRzMDk4M2JrNFJqWUZEM2dyTmpOWTZHNHByRDVrRExsSGlEMFVsVllsTU1XSnFWU2pkVmdBeGh2ZjdTcS1uMXJBWnNDRzN0QWlaYWVRaw\&q=https%3A%2F%2Feips.ethereum.org%2FEIPS%2Feip-4488\&v=65hxeeox1iI)

Sharding Improvements - [https://eips.ethereum.org/EIPS/eip-4844](https://www.youtube.com/redirect?event=video\_description\&redir\_token=QUFFLUhqbkd2a0ppV2ZHRVQzbWJCRnY2YnBPRGpJcjJtZ3xBQ3Jtc0ttQWF5ZFFKMGp1WjEyZ3BQUjRjb2R6MUtFM1dJOENJZ2M5d19KV054NmctODBFLTNrcThKRk90emtKM1JaWDJUWWhyc3JZQzFkUWtTc3dTMklMc043Y2ozUnczNGpNZVV4UHg2aWZlanBKOHk1enl0aw\&q=https%3A%2F%2Feips.ethereum.org%2FEIPS%2Feip-4844\&v=65hxeeox1iI)

