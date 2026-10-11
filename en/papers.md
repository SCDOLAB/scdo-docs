# Papers

Research from 9Y9 PTY LTD, trading as SCDO Laboratory. All papers are open-access preprints on Zenodo under CC BY 4.0. Papers page: https://scdoscan.io/papers/

Author: Ying Willam Zhang ([ORCID 0009-0002-1526-3332](https://orcid.org/0009-0002-1526-3332)), 9Y9 PTY LTD, trading as SCDO Laboratory.

## Agent Ledger

**SCDO Agent Ledger: On-Chain Identity, Work Attestation and Settlement for Autonomous AI Agents on a Sharded PoW Blockchain**

* First published 3 October 2026 (preprint, Zenodo).
* DOI (all versions): [10.5281/zenodo.23119809](https://doi.org/10.5281/zenodo.23119809)
* Page and PDF: https://scdoscan.io/papers/agent-ledger/

> Agentic AI systems composed of multiple large-language-model (LLM) agents need verifiable agent identity, tamper-evident records of completed work, and machine-to-machine settlement. […] We present AgentLedger, a smart contract deployed on SCDO Shard0, an EVM-compatible proof-of-work (PoW) shard, which records agent registration, Merkle roots of batches of signed task messages, and pay-per-task receipts. Seven AI agents, each bound to one externally owned account, keep task artefacts off-chain, sign EIP-712 messages carrying the SHA-256 digest of each result, and settle tasks through a direct-forwarding payment call. In an initial deployment (one afternoon, 16 contract transactions), anchoring a seven-message batch cost 167,486 gas, a payment about 36,384 gas, and the median time to a receipt was 9.0 s. *(abstract excerpt)*

## Mining pools

**Hashrate-Tiered Fees and PPLNS Settlement for Home-Miner Pools on a Sharded Proof-of-Work Blockchain: Design, Deployment and Simulation on SCDO**

* Published 4 October 2026 (preprint, Zenodo).
* DOI: [10.5281/zenodo.23209817](https://doi.org/10.5281/zenodo.23209817)
* Page, PDF and supplementary material: https://scdoscan.io/papers/mining-pools/

> […] We present two mining pools that are running in production on the SCDO sharded proof-of-work blockchain and that pay miners automatically on chain under Pay-Per-Last-N-Shares (PPLNS) accounting with hashrate-tiered fees of 5 %, 3 % and 1 %. The first pool serves GPU miners on SCDO Shard0, an EVM-compatible Ethash shard (chain ID 5680). The second, zpool, is a purpose-built Go pool for CPU miners on SCDO Classic Shard1, whose zpow algorithm rewards finding a large determinant of a 30 × 30 matrix derived from the block header. Because the work behind a zpow share does not grow linearly with share difficulty, zpool weights every share by its empirically measured expected number of hashes. *(abstract excerpt; the full abstract reports production records and a Monte-Carlo simulation)*

## GPU Share

**Verifiable Home-GPU Compute Sharing with Duplicate-Dispatch Checks and Merkle-Anchored Receipts on a Sharded PoW Chain**

* Published 7 October 2026 (preprint, Zenodo).
* DOI: [10.5281/zenodo.23209839](https://doi.org/10.5281/zenodo.23209839)
* Page and PDF: https://scdoscan.io/papers/gpu-share/

> This paper describes scdo-gpu-share, a worker and coordinator system in which each worker is identified only by a secp256k1 key address and runs deterministic llama.cpp and Blender jobs. Results are compared by SHA-256 under duplicate dispatch. […] Result batches are anchored as Merkle roots in the AgentLedger contract on SCDO Shard0 (chainId 5680), and only completed and anchored results are paid in the native unit SCDO. *(abstract excerpt)*

## Whitepaper

SCDO does not publish a separate whitepaper. This documentation is the technical overview: start with [What is SCDO?](README.md), [Networks and shards](getting-started/networks.md), [Tokenomics](tokenomics/README.md), [Mining overview](mining/README.md) and [Security practices](security/security.md).

## How to cite

Use the DOI of the paper. Zenodo provides BibTeX and other formats on each record page.
