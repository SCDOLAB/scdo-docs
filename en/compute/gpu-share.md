# GPU Share

**In development — coming soon.** GPU Share is not open for general use yet.

GPU Share is a design by 9Y9 PTY LTD, trading as SCDO Laboratory, for idle home NVIDIA GPUs to contribute verifiable compute, with results recorded on SCDO Shard0 EVM. The design is described in the paper *Verifiable Home-GPU Compute Sharing with Duplicate-Dispatch Checks and Merkle-Anchored Receipts on a Sharded PoW Chain*, DOI [10.5281/zenodo.23209839](https://doi.org/10.5281/zenodo.23209839).

## Design (as described in the paper)

* **Identity:** each worker is identified only by its own secp256k1 key address. The key stays on the worker's computer; the worker only sends signatures.
* **Jobs:** deterministic llama.cpp and Blender jobs.
* **Verification by duplicate dispatch:** the first 20 jobs of every worker are always assigned twice, and 10% of later jobs are duplicated (never to a worker on the same public IP). Results are compared by SHA-256.
* **Receipts:** result batches are anchored as Merkle roots in the [Agent Ledger](agent-ledger.md) contract on Shard0 EVM.
* **Time sharing:** a 10/10-minute schedule shares time between the owner and the platform. Idle platform time goes to public-good computing (Folding@home, team SCDO Laboratory #1068523) or SCDO mining.

No earnings are promised.

{% hint style="warning" %}
9Y9 PTY LTD, trading as SCDO Laboratory, will never ask for a worker key, private key or recovery phrase. Download software only from https://scdoscan.io.
{% endhint %}
