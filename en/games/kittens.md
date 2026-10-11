# SCDO Kittens

SCDO Kittens are virtual collectibles on SCDO Shard0 EVM. Page: https://scdoscan.io/kittens/

**Virtual collectibles for SCDO games. Not an investment; no returns promised.**

## Claim

* One free Gen0 kitten per address; you pay network gas only.
* 9,000 Gen0 kittens can be claimed; 1,000 stay in the owner reserve.
* The daily claim cap starts at 300 per UTC day; the owner cannot raise it above 1,000.
* A `?ref=0x…` link can set your referrer once. You cannot refer yourself and two people cannot refer each other. Claiming pays nothing to anyone.

## Breed

* You must own both kittens. Each kitten can breed 8 times.
* A parent cannot breed with its child, and full siblings cannot breed.
* The breeding fee is paid when you breed. Birth uses the hash of a later block and anyone can finalize it; if 256 blocks pass first, the child is a baseline kitten.

## Market

* Listed kittens stay in your wallet until sold. Approve the market, then set a price in SCDO.
* Market fee: 4% by default; it can never exceed 10%.
* The seller is paid immediately. If that payment fails, the proceeds wait in the contract and you withdraw them yourself.
* Referral and treasury credits from breeding and market fees are withdrawn by their owners.

## Contracts (SCDO Shard0 EVM)

| Contract | Address |
| --- | --- |
| Kittens | `0x5d5210891A3929E4344226941A486282Fd1480Fc` |
| Registry | `0xc6Ea442E7Af84390aBaf80464B19698AfE30a4dE` |
| Market | `0xF0405642ebE3F962Dd4B37Ce16447E7Dc06d79fc` |

The current breeding fee is shown on https://scdoscan.io/kittens/ before you confirm.
