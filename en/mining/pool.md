# Project PPLNS pool (Shard0 EVM)

9Y9 PTY LTD, trading as SCDO Laboratory, runs a public PPLNS mining pool for Shard0 EVM. Every miner's hashrate, shares, blocks and payouts are public on https://scdoscan.io/pool/.

| Item | Value |
| --- | --- |
| Stratum | `stratum+tcp://82.223.19.88:3333` |
| Username | Your SCDO address (`0x…` or `0x….rigname`) |
| Example | `rigel -a ethash -o ethproxy+tcp://82.223.19.88:3333 -u 0xYOUR_ADDRESS -w rig1` |
| Payout scheme | PPLNS: each block reward is shared over the last 1 G of accepted share difficulty |
| Minimum payout | 1 SCDO, after 64 blocks of maturity; the pool pays the network fee |
| Pool wallet | `0x675E8639A73ECFe13561DbABc25e56CB82088D24` |

## Fees

The fee depends on your 24-hour average hashrate. All fees go to the reserve address `0x42c4854A51127f2D9D770f0d4AECa0683f72c0e4`.

| Tier | 24 h average hashrate | Fee |
| --- | --- | --- |
| Large | ≥ 500 MH/s | 1% |
| Medium | 100–500 MH/s | 3% |
| Small | < 100 MH/s | 5% |

Solo mining with your own node remains fully supported and has no pool fee.

The design and simulation of this pool are described in the paper [Hashrate-Tiered Fees and PPLNS Settlement for Home-Miner Pools](../papers.md#mining-pools).
