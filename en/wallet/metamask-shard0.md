# Add SCDO Shard0 (EVM) to MetaMask

SCDO Shard0 (EVM) is an EVM-compatible proof-of-work network with chain ID 5680. MetaMask can connect to it when the network details are entered correctly. Use only the values on this page, check the domain before connecting, and never share your private key or Secret Recovery Phrase.

## Before you begin

Install MetaMask only from the official source at https://metamask.io/. Do not install a wallet extension from a pop-up, an unsolicited message or a look-alike website. A fake extension can capture your password or recovery information.

## Option 1: one click

1. Open https://scdoscan.io/start.html yourself (type it or use a bookmark).
2. Select **Add SCDO Shard0 (EVM) to MetaMask**.
3. Review the request in MetaMask and approve it. MetaMask switches to SCDO Shard0 (EVM).

On the MetaMask mobile app, open https://scdoscan.io/start.html inside the app's built-in browser and tap the same button.

## Option 2: manual setup

Open the MetaMask network menu. Current releases may show **Manage networks**, then **Add a custom network**. Other releases show **Settings > Networks > Add network > Add a network manually**. The labels can differ slightly between versions; the goal is to open the custom network form, not to pick an unknown suggested network.

Enter each value exactly:

| Field | Value |
| --- | --- |
| Network name | `SCDO Shard0 (EVM)` |
| RPC URL | `https://scdoscan.io/rpc/0` |
| Chain ID | `5680` |
| Currency symbol | `SCDO` |
| Block explorer URL | `https://scdoscan.io` |

* **RPC URL:** check the `https` prefix, the exact `scdoscan.io` domain and the final `/0`. Do not use an RPC copied from a comment, a direct message or an ad.
* **Chain ID:** `5680` (hexadecimal `0x1630`), with no extra spaces or digits.
* **Block explorer URL:** `https://scdoscan.io`, with no tracking parameter and no similar-looking domain.

Read the five entries back before saving, then select **Save** and switch to **SCDO Shard0 (EVM)** in the network selector.

Adding a network never requires your recovery phrase or private key. Do not approve an unexpected connection or signature request just because a network was added.

## Shard0 and Classic addresses

Your SCDO Shard0 (EVM) account uses a standard EVM address beginning with `0x`, the same address you have on other EVM networks.

SCDO Shard1 (Classic) through SCDO Shard4 (Classic) use Classic addresses such as `1S01...` and `2S02...`, with 8 decimal places. Classic addresses do not work in MetaMask. Use the SCDO Web Wallet at https://scdoscan.io/wallet/ or the desktop [SCDO Wallet](https://scdoscan.io/downloads/wallet/) for those accounts.

## Check on the explorer

Open a new tab and type https://scdoscan.io yourself. Check that the address bar shows exactly `scdoscan.io` over HTTPS. Paste your `0x` address into the search box to see its SCDO Shard0 (EVM) balance and history.

Watch for fake RPC endpoints, look-alike sites and unexpected signature requests. No genuine setup guide needs your private key or Secret Recovery Phrase.

## Final checklist

* MetaMask came from https://metamask.io/.
* The network is SCDO Shard0 (EVM).
* The RPC URL is https://scdoscan.io/rpc/0.
* The chain ID is 5680.
* The symbol is SCDO and the explorer is https://scdoscan.io.
* Your recovery information stays private.

These are network connection instructions. SCDO tokens have no promised market value. No promise of block reward or market value.
