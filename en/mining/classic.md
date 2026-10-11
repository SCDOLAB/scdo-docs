# Classic shards

SCDO Shard1 (Classic) to SCDO Shard4 (Classic) are SCDO's original core chain (go-scdo, ZPoW algorithm, `1S01…` addresses). You can mine 1, 2, 3 or all 4 shards; all four together is recommended.

## Options

* **GPU, Shard1 pool:** `stratum+tcp://82.223.19.88:3341`, username = your `1S01…` address. GPU miner: zminer-gpu.
* **CPU, easiest:** use the built-in mining in SCDO Wallet for Windows (https://scdoscan.io/downloads/wallet/) and click **Start mining**.
* **Solo:** run your own Classic node (Linux binaries `scdo-node` and `scdo-client` on https://scdoscan.io/mine/, source `SCDOLAB/go-scdo`).

A fresh node starts at the fork genesis (about block 2.98 million) and syncs forward. A full node for all chains needs about 118 GB of disk.

Classic-shard SCDO is separate from Shard0 EVM SCDO and cannot be bridged or moved to Shard0. The design of the Shard1 pool is described in the [mining-pools paper](../papers.md#mining-pools).
