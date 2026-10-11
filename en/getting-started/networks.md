# Networks and shards

## SCDO Shard0 EVM

| Field | Value |
| --- | --- |
| Network name | `SCDO Shard0 EVM` |
| Chain ID / network ID | `5680` (hex `0x1630`) |
| RPC URL | `https://scdoscan.io/rpc/0` |
| Backup RPC URL | `https://apeccapital.org/rpc/0` |
| Currency symbol | `SCDO` |
| Decimals | 18 |
| Block explorer | `https://scdoscan.io` |
| Consensus | Ethash proof-of-work (same as pre-merge Ethereum; 30,000-block epochs; not etchash) |
| Client | core-geth v1.12.23 (SCDO fork) |
| Block target | about 13 seconds |
| Gas limit | 30,000,000 |
| Fee model | EIP-1559 active from block 0; base fee burned |
| P2P port | 30368 |
| ChainList | https://chainlist.org/chain/5680 |

### Notes for developers

* Set Solidity `evmVersion` to **`paris`**. Shanghai and later opcodes (`PUSH0`, `MCOPY`, `TLOAD`, `TSTORE`) are not enabled on Shard0 EVM.
* Send **legacy (type-0)** transactions.
* Shard0 nodes can follow company-signed checkpoints. See [Security practices](../security/security.md#signed-checkpoints).

## SCDO Classic shards

SCDO Shard1 (Classic), Shard2 (Classic), Shard3 (Classic) and Shard4 (Classic) form SCDO's own original core chain.

| Item | Value |
| --- | --- |
| Client | go-scdo (source: GitHub `SCDOLAB/go-scdo`) |
| Algorithm | ZPoW |
| Address format | `1S01...` (Shard1), `2S02...` (Shard2), and so on |
| Decimals | 8 |
| Wallets | SCDO Web Wallet (https://scdoscan.io/wallet/) and desktop SCDO Wallet; not MetaMask |
| Accounts | over 240,000 user accounts, searchable on the explorer |

The Classic chain is a fork whose genesis is at about block 2.98 million, so a fresh node starts there and syncs forward. A full node for all chains needs about 118 GB of disk.

## Classic SCDO and Shard0 EVM SCDO are separate

SCDO on the Classic shards (Shard1–4) and SCDO on Shard0 EVM are separate balances on separate chains. Classic-shard SCDO cannot be bridged or moved to Shard0 EVM, and the two are not currently interchangeable.

{% hint style="warning" %}
Always check that the sender uses the same network as your address. A `0x` address and a `1S01...` address are on different chains.
{% endhint %}
