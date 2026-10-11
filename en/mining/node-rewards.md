# Node rewards

Public, synced SCDO Shard0 EVM nodes serve the network and receive node rewards in SCDO under public rules based on measured online time and contribution.

## How to register

Add this flag to your node command (the GPU package v1.0.3 and the macOS `start.sh` do it for you):

```
--identity scdo-node:0xYOUR_ADDRESS
```

The bootnode (`82.223.19.88:30368`) uses it to know which address receives your node rewards.

## Rules (node reward v2, in effect from the UTC day 2026-10-10)

* Servers check every 5 minutes which registered nodes are connected and at the chain head.
* Rewards are split by each node's contribution share.
* The daily reward pool has a floor of **100 SCDO per UTC day**.
* The day closes at 00:00 UTC (08:00 UTC+8); results are published around 08:45 UTC+8. If no node qualifies, the pool rolls over to the next day.
* Every payout is manually confirmed and signed by the project; the server does not send payouts automatically.
* Project nodes are shown for transparency and are not included in distributions.

Node list, full rules, daily ledger and distributions: https://scdoscan.io/nodes/. The rules published there are authoritative.

No income is promised.
