# Install the GPU Share worker

GPU Share worker 1.2.4 lets an idle NVIDIA graphics card compute while your PC is not in use. It needs no wallet, no node and no signup: download, unzip, double-click.

**Requirements:** Windows 10/11 64-bit and an NVIDIA GPU with 4GB VRAM or more.

## Step 1: Download and check the file

1. Open https://scdoscan.io/gpu-share/?ref=gitbook and download the Windows zip, `scdo-gpu-share-worker-1.2.4-win-x64.zip`.
2. Check the file before you run anything. In PowerShell, in the folder that holds the zip:

```powershell
Get-FileHash .\scdo-gpu-share-worker-1.2.4-win-x64.zip -Algorithm SHA256
```

The result must be exactly:

```
96e19a186a53e42c59bd67c00244afff166acf03df1e80ba62a90cc55c8880f4
```

If it does not match, delete the file and download it again from https://scdoscan.io/gpu-share/?ref=gitbook only.

## Step 2: Unzip

Extract the zip to any folder, for example `C:\scdo-gpu-share\`. You can move the folder or unzip again later: your key is stored separately, so your address stays the same.

## Step 3: Double-click

Double-click `scdo-gpu-share-worker-1.2.4-win-x64.exe`.

If Windows shows "Windows protected your PC": the program does not have a code-signing certificate, so Windows may show this warning. After you have checked the SHA-256, click **More info**, then **Run anyway**.

That is all. The worker asks for nothing. On first start it creates your worker key and your 0x payout address on SCDO Shard0 (EVM). While the PC is idle it mines SCDO first: Rigel, from the official miner package, connects straight to the public SCDO pool with your address. Rigel is closed source and takes a 0.7% dev fee. If mining cannot start, the official Folding@home client takes over and runs medical research as part of team SCDO Laboratory (#1068523).

## Back up your key

{% hint style="warning" %}
On first start the worker creates `worker.key` in `%APPDATA%\SCDO\gpu-share`. The 0x address of this private key is your payout address.

* Back up `%APPDATA%\SCDO\gpu-share\worker.key` right away, for example to a USB drive you keep offline.
* Never share this file with anyone. SCDO Laboratory will never ask for it.
* Anyone who has this file controls the address.
{% endhint %}

To open the folder, press **Win + R**, type `%APPDATA%\SCDO\gpu-share` and press Enter.

## Reinstalling or moving the folder

Your key lives in `%APPDATA%\SCDO\gpu-share`, not in the program folder. Reinstalling, unzipping into a new folder or moving the folder keeps the same worker and the same address, as long as you do not delete `%APPDATA%\SCDO\gpu-share`.


## Check your worker

Enter your worker address in "Check your worker" at https://scdoscan.io/gpu-share/?ref=gitbook#check, or search the address on https://scdoscan.io to see its on-chain records.

## Stop or remove

* **Stop:** close the program window, or end `scdo-gpu-share-worker-1.2.4-win-x64.exe` in Task Manager. It does not install a Windows service.
* **Remove:** delete the unzipped folder. To remove everything, also delete `%APPDATA%\SCDO\gpu-share` (and `%AppData%\scdo-gpu-worker` if it exists). Back up `worker.key` first if you may return.

More questions: see the [GPU Share FAQ](faq.md).

For information only. Not financial advice. SCDO tokens have no promised market value. No promise of block reward or market value.
