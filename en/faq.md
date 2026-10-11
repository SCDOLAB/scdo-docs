# FAQ

## What is SCDO?

A sharded proof-of-work blockchain network: SCDO Shard0 EVM (chain ID 5680, Ethash, EVM-compatible) plus the Classic shards Shard1–4 (go-scdo, ZPoW). See [What is SCDO?](README.md).

## Who runs it?

9Y9 PTY LTD, trading as SCDO Laboratory (ABN 19 600 445 118), Melbourne, Victoria, Australia. AUSTRAC DCE100714503-001, AFCA 124589. See [Company and compliance](security/compliance.md).

## Which network settings do I use?

Network name `SCDO Shard0 EVM`, chain ID `5680` (`0x1630`), RPC `https://scdoscan.io/rpc/0`, symbol `SCDO`, explorer `https://scdoscan.io`. Backup RPC: `https://apeccapital.org/rpc/0`.

## Where do I download SCDO Wallet?

Only from https://scdoscan.io/downloads/wallet/.

## How do I back up my wallet?

Windows and Mac: back up the account file (`%USERPROFILE%\.ScdoWallet\account` or `~/.ScdoWallet/account`) and its password. Android and the web wallet: write down the recovery phrase on paper. Never share either. See [SCDO Wallet](getting-started/wallet.md).

## Does my 0x address work on the Classic shards?

No. Classic shards use `1S01…`-style addresses and are not supported by MetaMask. Use the SCDO Web Wallet or the desktop SCDO Wallet.

## Can I move Classic-shard SCDO to Shard0 EVM?

No. Classic-shard SCDO (Shard1–4) and Shard0 EVM SCDO are separate. Classic SCDO cannot be bridged or moved to Shard0, and the two are not currently interchangeable.

## Is there a maximum supply?

There is currently no fixed maximum supply and no halving. SCDO is issued at 2 SCDO per block.

## Is there a whitepaper?

This documentation is SCDO's technical overview; there is no separate whitepaper. Research papers are listed on [Papers](papers.md).

## Was there a presale or premine?

No presale. The genesis carries over balances from the earlier Shard0 chain plus a 100 SCDO faucet allocation, and nothing else. See [SCDO](tokenomics/scdo.md#genesis).

## What is the total supply?

It is computed from the chain block by block and shown live on https://scdoscan.io/transparency/.

## What are WSCDO and SCDOR?

WSCDO is SCDO wrapped 1:1 as an ERC-20. SCDOR is the capped in-app reward token for SCDO games and programs. See [Tokenomics](tokenomics/README.md).

## How do I mine?

Solo with your own node, through the project PPLNS pool, or with the built-in miner in SCDO Wallet for Windows. See [Mining overview](mining/README.md).

## How much will I earn?

No income is promised. Rewards depend on your hashrate, network difficulty and luck, and SCDO has no promised market value.

## Where are the technical papers?

See [Papers](papers.md) and https://scdoscan.io/papers/.

## I found a bug.

Report it to https://t.me/SCDOLabor. See [Bug bounty](games/wheel.md#bug-bounty).

## How do I get help?

Telegram community: https://t.me/SCDOCommunity. Email: admin@apeccapital.org. Never share your recovery phrase or private key with anyone offering help.
