# Security practices

## Your keys

* SCDO Wallet is non-custodial. Keys, recovery phrases and account files stay on your device.
* 9Y9 PTY LTD, trading as SCDO Laboratory, will **never** ask for your private key, recovery phrase, account file, password or `worker.key`.
* Download software only from https://scdoscan.io and check the published SHA-256 before running it. A server-side job recomputes the SHA-256 of every file under `/downloads/` every 15 minutes and compares it with the published `SHA256SUMS` (see the Transparency Center).
* Type https://scdoscan.io yourself. Watch for look-alike domains, fake RPC endpoints and unexpected signature requests.

## Signed checkpoints

Every 20 blocks, once a block is 12 blocks deep, the company signs its number and hash. Upgraded Shard0 nodes reject any chain that does not contain the signed block, so a hidden chain built with rented hashrate cannot rewrite blocks older than the latest checkpoint. Nodes report the signed block as `finalized` over RPC. Peers that keep sending conflicting chains are temporarily banned (10 minutes, doubling up to 24 hours).

| Item | Value |
| --- | --- |
| Signer | `0xee028b0fD3e852aa7126A2b66Ada01d578F40f57` |
| Policy | 1-of-1 signature, every 20 blocks, 12 confirmations |
| Latest checkpoint | https://scdoscan.io/checkpoint/shard0/latest.json |
| Signed message | `SCDO-CHECKPOINT-v1 chainId=5680 number=<n> hash=<0x…>` (EIP-191 `personal_sign`) |

Enable on your node:

```
--scdo.checkpoint.signers 0xee028b0fD3e852aa7126A2b66Ada01d578F40f57 \
--scdo.checkpoint.url https://scdoscan.io/checkpoint/shard0/latest.json \
--scdo.checkpoint.poll 15s
```

Verify yourself: `scdocheckpoint verify -file latest.json -signers 0xee028b0fD3e852aa7126A2b66Ada01d578F40f57 -chainid 5680`, or recover the signer with any EIP-191 tool and compare the hash with `eth_getBlockByNumber` on your own node.

**Trust note:** a node that enables checkpoints trusts this signer for finality. The signer cannot create coins, move funds or change balances; it can only confirm which block is final. Nodes without the checkpoint flags keep plain proof-of-work rules.

## Transparency

The [Transparency Center](https://scdoscan.io/transparency/) publishes who mines Shard0 EVM, total supply and its formula, genesis allocations, company addresses, core software versions and node counts. Raw data: https://scdoscan.io/transparency/data.json

## Open source

| Repository (GitHub `SCDOLAB`) | Contents |
| --- | --- |
| `scdo-shard0` (branch `scdo`) | Shard0 EVM node: core-geth v1.12.23 fork + scdo-stratum proxy |
| `scdo-gpu-miner` | GPU mining package |
| `go-scdo` | Classic shard node |
| `scdoscan-web`, `scdoscan-api` | Explorer and web wallet |
| `scdowallet` | Desktop wallet |
| `chains` | Chain metadata |

## Report a vulnerability

See [Bug bounty](../games/wheel.md#bug-bounty). Report to https://t.me/SCDOLabor and do not publish the issue before it is fixed.
