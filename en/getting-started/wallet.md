# SCDO Wallet

SCDO Wallet is the non-custodial wallet app of 9Y9 PTY LTD, trading as SCDO Laboratory. Private keys and recovery phrases are created and stored only on your device. SCDO Laboratory never receives or holds them and cannot move, freeze or recover your assets.

## Download

Download only from the official page: **https://scdoscan.io/downloads/wallet/**. Each file has a published SHA-256 checksum on that page.

Versions listed on the download page on 12 October 2026 (always use the latest version shown there):

| Platform | Version | Notes |
| --- | --- | --- |
| Windows 10/11 (x64) | 3.1.1 | Installs over older versions; accounts are kept. The only build with built-in GPU mining (NVIDIA, Shard0 EVM). |
| Android | 0.1.17 | APK from the website, or Google Play. The two versions cannot be installed over each other. |
| macOS (Apple silicon M1–M4) | 3.0.8 | Wallet only, no mining. |

## Check the file

Compare the SHA-256 of your download with the value on the download page:

* Windows: `certutil -hashfile <file> SHA256`
* macOS: `shasum -a 256 <file>`
* Linux: `sha256sum <file>`

## Install tips

* **Windows:** if you see "Windows protected your PC", click **More info**, then **Run anyway**.
* **macOS:** unzip, drag "SCDO Wallet" to Applications. If macOS cannot verify the developer, go to **System Settings → Privacy & Security → Open Anyway**.
* **Android:** allow "Install unknown apps" for the app you used to open the APK.

## Back up your wallet

{% hint style="warning" %}
* **Windows and Mac** show no recovery phrase. Your backup is the account file (Windows: `%USERPROFILE%\.ScdoWallet\account`, Mac: `~/.ScdoWallet/account`) plus its password.
* **Android and the web wallet:** write the recovery phrase on paper in the exact order shown and keep it offline.
* Never share the file, the password or the phrase. Staff of 9Y9 PTY LTD, trading as SCDO Laboratory, will never ask for them. Lost backups cannot be recovered.
{% endhint %}

## Networks

The wallet opens on SCDO Shard0 EVM. The desktop wallet also supports the Classic shards (`1S01...` addresses). See [Networks and shards](networks.md).

## Mining (Windows)

The Windows wallet can mine SCDO Shard0 EVM on NVIDIA GPUs. Stop mining with the wallet's **Stop** button. If your antivirus removes the mining program, add the wallet folder to its exclusion list. The miner is Rigel (closed source, 0.7% developer fee). See [Mining overview](../mining/README.md).

## Tokens

SCDO is shown first. WSCDO and SCDOR are tokens on Shard0 EVM; their contract addresses are listed in [Tokenomics](../tokenomics/README.md). Always copy addresses from the official documentation or explorer, never from a chat message.
