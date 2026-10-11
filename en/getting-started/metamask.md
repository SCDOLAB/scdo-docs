# Add SCDO Shard0 EVM to MetaMask

## Option 1: one click

1. Open https://scdoscan.io/metamask/ (or https://scdoscan.io/start.html) yourself.
2. Click the add-network button and approve the request in MetaMask.

On MetaMask Mobile, open the page in the app's built-in browser.

## Option 2: manual setup

In MetaMask, open the custom network form (**Manage networks → Add a custom network**, or **Settings → Networks → Add a network manually**, depending on the version) and enter:

| Field | Value |
| --- | --- |
| Network name | `SCDO Shard0 EVM` |
| RPC URL | `https://scdoscan.io/rpc/0` |
| Chain ID | `5680` |
| Currency symbol | `SCDO` |
| Block explorer URL | `https://scdoscan.io` |

Check the `https` prefix, the exact `scdoscan.io` domain and the final `/0`. Do not use an RPC copied from a comment, DM or ad.

Adding a network never requires your recovery phrase or private key.

## Classic addresses

`1S01...` / `2S02...` Classic addresses do not work in MetaMask. Use the SCDO Web Wallet (https://scdoscan.io/wallet/) or the desktop [SCDO Wallet](wallet.md).
