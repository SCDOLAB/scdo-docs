# What is SCDO?

SCDO is a sharded proof-of-work (PoW) blockchain network operated and developed by **9Y9 PTY LTD, trading as SCDO Laboratory** (Melbourne, Victoria, Australia).

The network has two parts:

* **SCDO Shard0 EVM**: an EVM-compatible Ethash proof-of-work chain (chain ID **5680**) running on core-geth, the Ethereum Classic client. It uses standard `0x` addresses and works with MetaMask and other EVM tools.
* **SCDO Shard1 (Classic) to SCDO Shard4 (Classic)**: SCDO's own original core chain (go-scdo, ZPoW algorithm), with addresses such as `1S01...`. It is live, with over 240,000 user accounts searchable on the explorer.

The two parts are separate chains: Classic-shard SCDO cannot be bridged or moved to Shard0 EVM, and the two are not currently interchangeable.

Anyone can mine with a GPU, run a full node, and check every block, transaction and reward on the public explorer at [scdoscan.io](https://scdoscan.io).

## What we build on the network

| Product | What it is | Status |
| --- | --- | --- |
| [SCDO Wallet](getting-started/wallet.md) | Non-custodial wallet for Windows, macOS (Apple silicon) and Android, plus a web wallet | Live |
| [SCDO Scan](https://scdoscan.io) | Block explorer, public RPC and transparency center | Live |
| [Mining and node rewards](mining/README.md) | Solo mining, a public PPLNS pool and rewards for public full nodes | Live |
| [Agent Ledger](compute/agent-ledger.md) | On-chain identity, signed work logs and settlement for AI agents | Live (experimental) |
| [GPU Share](compute/gpu-share.md) | Design for verifiable compute on idle home GPUs | In development |
| [Games](games/README.md) | Thank-you wheel, Shard Miner, SCDO Kittens | Live |
| [didiATM](didiatm.md) | Peer-to-peer cash and crypto exchange network with on-chain escrow | In development |
| [Papers](papers.md) | Open-access research preprints on Zenodo | Published |

This documentation is SCDO's technical overview; there is no separate whitepaper.

## Quick facts

| Item | Value |
| --- | --- |
| Main network | SCDO Shard0 EVM |
| Chain ID | 5680 (`0x1630`) |
| Consensus | Ethash proof-of-work |
| Native coin | SCDO (18 decimals on Shard0 EVM) |
| Block reward | 2 SCDO per block, plus standard Ethash uncle rewards |
| Fee model | EIP-1559: the base fee is burned, the priority fee goes to the miner |
| Current chain start | 28 September 2026 |
| RPC | `https://scdoscan.io/rpc/0` (backup `https://apeccapital.org/rpc/0`) |
| Transactions | Legacy (type-0) transactions |
| Explorer | https://scdoscan.io |

Live figures (block height, total supply, hashrate, top miners) are published on the [Transparency Center](https://scdoscan.io/transparency/) and recomputed every 5 minutes.

## Start here

* [Getting started](getting-started/README.md)
* [Tokenomics](tokenomics/README.md)
* [Mining](mining/README.md)
* [Company and compliance](security/compliance.md)

{% hint style="info" %}
SCDO tokens have no promised market value. There is no promise of block reward or market value. Nothing in this documentation is financial advice.
{% endhint %}
