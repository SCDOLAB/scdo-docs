# Mining overview

SCDO is a proof-of-work network. Miners bundle transactions into blocks and make history expensive to rewrite; independent full nodes check every block and serve the network.

## Ways to take part

| Option | Network | Hardware | Rewards go to | Fee |
| --- | --- | --- | --- | --- |
| [Solo mining with your own node](shard0-gpu.md) | Shard0 EVM | NVIDIA GPU (Windows/Linux) | Your address, directly | No pool fee |
| [Project PPLNS pool](pool.md) | Shard0 EVM | Any Ethash GPU miner | Your address, via pool payouts | 1% / 3% / 5% by hashrate |
| Built-in mining in SCDO Wallet for Windows | Shard0 EVM | NVIDIA GPU | Your `0x` address | See wallet |
| [Classic pool or solo](classic.md) | Shard1–4 (Classic) | GPU or CPU | Your `1S01...` address | See page |
| [Run a public node](node-rewards.md) | Shard0 EVM | Always-on PC or server | Your address, via node rewards | None |

## Before you start

* You need a PC or server (Windows or Linux) that can stay online; phones are not suitable. The Mac app is wallet only.
* Mining uses electricity and hardware. Block rewards, pool payouts and node rewards follow public rules and can be checked on the explorer, on https://scdoscan.io/pool/ and on https://scdoscan.io/nodes/.
* The bundled NVIDIA miner, Rigel, is third-party, closed source and takes a 0.7% developer fee.
* Only download node software from https://scdoscan.io (checksums provided) or build it yourself. Never enter a recovery phrase into mining or node software.

No income is promised. Rewards depend on your hashrate, the network difficulty and luck.
