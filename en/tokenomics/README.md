# Tokenomics overview

SCDO Shard0 EVM has one native coin and two contract tokens:

| Asset | Type | Address | Decimals | Role |
| --- | --- | --- | --- | --- |
| **SCDO** | Native coin of Shard0 EVM | native | 18 | Gas, mining and node rewards, payments |
| **WSCDO** (Wrapped SCDO) | ERC-20, WETH9 design | `0x5c2d19142f021375D9f440Ed441015e59E28Ab29` | 18 | 1:1 wrapped SCDO for use in contracts and the Shard0 DEX |
| **SCDOR** (SCDO Reward) | ERC-20, capped | `0xd76C042a0DbA95E0B9d302d33849304CbD4E5fc3` | 18 | In-app reward token for SCDO games and programs |

All three are on SCDO Shard0 EVM (chain ID 5680). Check any address on https://scdoscan.io.

The Classic shards (Shard1–4) have their own SCDO balances (8 decimals). Classic-shard SCDO is separate from Shard0 EVM SCDO: it cannot be bridged or moved to Shard0, and the two are not currently interchangeable.

## Principles

* **No presale.** There was no token sale for SCDO.
* **No premine beyond the published genesis.** The genesis file carries over balances from the earlier Shard0 chain plus a 100 SCDO faucet allocation; see [SCDO](scdo.md#genesis).
* **Supply is computed from the chain, block by block**, not estimated, and published on the [Transparency Center](https://scdoscan.io/transparency/).
* **No fixed maximum supply.** SCDO is issued at 2 SCDO per block. There is currently no fixed max supply or halving.
* **No promised value or returns.** SCDO, WSCDO and SCDOR have no promised market value. SCDOR is a reward token for in-app use and is not an investment.

## Pages

* [SCDO (native coin)](scdo.md)
* [WSCDO (Wrapped SCDO)](wscdo.md)
* [SCDOR (SCDO Reward)](scdor.md)
* [Shard0 DEX contracts](dex.md)
