# SCDO (native coin)

SCDO is the native coin of SCDO Shard0 EVM. It pays for gas and is created only by mining under public protocol rules.

## Issuance

| Item | Value |
| --- | --- |
| Block reward | 2 SCDO per block |
| Uncle rewards | Standard Ethash rules: `(uncle_number + 8 − block_number) / 8 × 2 SCDO` to the uncle miner, plus `2 SCDO / 32` per included uncle to the block miner |
| Fee burn | EIP-1559 base fee (`baseFeePerGas × gasUsed`) is burned |
| Priority fee | Goes to the block miner |
| Block target | about 13 seconds |

There is currently no fixed maximum supply and no halving. New SCDO is issued at 2 SCDO per block (plus uncle rewards), and part of every transaction fee is burned.

## Total supply

Total supply is computed from the chain, block by block:

```
total = genesis allocations
      + 2 SCDO × block height                                  (block rewards)
      + Σ (uncle_number + 8 − block_number) / 8 × 2 SCDO       (uncle rewards)
      + uncles × 2 SCDO / 32                                   (uncle inclusion rewards)
      − Σ baseFeePerGas × gasUsed                              (burned base fees)
```

The live value is on the [Transparency Center](https://scdoscan.io/transparency/) and in its raw data file https://scdoscan.io/transparency/data.json, recomputed every 5 minutes. You can check any block, address and transaction on the explorer at https://scdoscan.io.

## Genesis

The current Shard0 EVM chain started on **28 September 2026**. Its genesis file (downloadable from the Transparency Center) carries over balances from the earlier SCDO Shard0 EVM chain (final block 74,023); the faucet received a new 100 SCDO allocation. The genesis file and its total are published on the Transparency Center. There is no other premine and no presale.

## Who mines today

The Transparency Center states plainly that **today the company's own machines and the project-run pool produce most Shard0 EVM blocks**. It lists the top miners for the last 1,000 blocks and all time. Independent miners are welcome: the more of them, the more decentralised the network becomes.

## Company addresses (public)

| Address | Role |
| --- | --- |
| `0x42c4854A51127f2D9D770f0d4AECa0683f72c0e4` | Company reserve (9Y9 PTY LTD, trading as SCDO Laboratory): project-operated mining (company GPUs); receives pool fees and the wheel withdrawal fee; funds node rewards and the faucet |
| `0x675E8639A73ECFe13561DbABc25e56CB82088D24` | Project PPLNS pool wallet: receives pool block rewards and pays miners |
| `0xb51199e09c98d0a797629519a049db7954f04381` | scdoscan.io server node (CPU mining); also the genesis coinbase |
| `0x0889453fE946c75163B3BbdF2266f2566B2f4c03` | Node reward distribution wallet (holds only what the reserve puts in) |

## What SCDO is used for

* Gas on Shard0 EVM.
* Mining pool payouts and node rewards.
* Agent-to-agent task settlement in the [Agent Ledger](../compute/agent-ledger.md).
* Breeding and market fees in [SCDO Kittens](../games/kittens.md).
* Membership (see https://scdoscan.io/membership/).

SCDO has no promised market value. Nothing here is financial advice.
