# SCDOR (SCDO Reward)

SCDOR is the in-app reward token for SCDO games and programs. It is **not an investment and no returns are promised**.

| Item | Value |
| --- | --- |
| Name / symbol | SCDO Reward / SCDOR |
| Address | `0xd76C042a0DbA95E0B9d302d33849304CbD4E5fc3` |
| Network | SCDO Shard0 EVM (chain ID 5680) |
| Decimals | 18 |
| Supply cap | 10,000,000 SCDOR, enforced on every mint. The owner can only lower the cap, never raise it. |
| Current supply | 300 SCDOR (on-chain `totalSupply`; live value on https://scdoscan.io) |
| Deployed | 11 October 2026, block 98,933 (tx `0x15c389bc58c44168343d6f39d0f7377b894668578565722aec3f08b00a9dc246`) |
| Compiler | solc 0.8.24, EVM paris, optimizer 200 runs |

## Contract features

* ERC-20 with burn.
* `Ownable2Step` ownership; renouncing ownership is disabled.
* The owner appoints minters with `setMinter(address, bool)`.
* `mint` and `mintBatch(batchId, ...)`; each `batchId` can be settled only once, which prevents double minting.
* The supply cap is checked on every mint.

## Liquidity

An SCDOR / WSCDO pool exists on the [Shard0 DEX](dex.md):

* Pair: `0x18C4630300595Ce6B4449D643F8aF06a45e6a4b8`
* The pool was seeded by 9Y9 PTY LTD, trading as SCDO Laboratory.
* Live reserves are shown on https://scdoscan.io/kittens/ (section "SCDOR / WSCDO pool") and on the explorer.

SCDOR is minted only by addresses the owner appoints, never above the cap.
