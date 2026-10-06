# GPU Share FAQ

## Do I need to sign up or verify my identity?

No. No KYC, no email, no signup form. Download, unzip, double-click. See [Install the worker](install.md).

## Do I need a wallet first?

No. On first start the program creates `%APPDATA%\SCDO\gpu-share\worker.key`. The 0x address of that key is your payout address. Back the file up right away and never share it.

## Where do I see my address?

Enter it in "Check your worker" at https://scdoscan.io/gpu-share/?ref=gitbook#check, or search the address on https://scdoscan.io to see its on-chain records.

## Will reinstalling or moving folders change my address?

No. The key is stored in `%APPDATA%\SCDO\gpu-share`. As long as you don't delete that folder, a reinstall is the same worker with the same address.

## What hardware do I need?

Windows 10/11 64-bit and an NVIDIA GPU with 4GB VRAM or more.

## Which systems are supported?

Windows and Linux both support idle mining and Folding@home. The download page currently offers the Windows download.

## What does it do while my PC is idle?

It mines SCDO first: Rigel, from the official miner package, connects straight to the public SCDO pool with your address, so no local node is needed. Rigel is closed source and takes a 0.7% dev fee. If mining cannot start, the official Folding@home client takes over and contributes to medical research as part of team SCDO Laboratory (#1068523).

## How much resource does it use?

The worker alternates 10-minute platform slots with 10-minute slots left for you. GPU load rises while it computes, so improve airflow if your case runs hot, or run it only while you're out or asleep. Close it before gaming.

## How do I stop it?

Close the window, or end `scdo-gpu-share-worker-1.2.4-win-x64.exe` in Task Manager. It does not install a Windows service.

## How do I uninstall?

Delete the unzipped folder. To remove everything, also delete `%APPDATA%\SCDO\gpu-share` (and `%AppData%\scdo-gpu-worker` if it exists). Back up `worker.key` first if you may return.

## Can I run several PCs on one network?

Yes, each PC creates its own address. Up to 20 active workers per public IP can register; workers offline for more than 7 days don't count. If registration is refused for now, the worker keeps mining and folding and retries by itself.

## Windows says "Windows protected your PC". Is it a virus?

No. The program does not have a code-signing certificate, so Windows may show this warning. Check the zip against the SHA-256 on the download page first, then click **More info**, then **Run anyway**.

## Is it safe? Does it send my data anywhere?

The private key stays on your computer; the worker only sends signatures. Check the SHA-256 before running. Payouts are ordinary SCDO Shard0 (EVM) transactions you can look up on https://scdoscan.io. The program is operated by 9Y9 PTY LTD (SCDO Laboratory), an Australian company.

## Where does the SCDO come from?

Three sources, none of them a promise of income:

1. **Paid jobs:** verified jobs are settled from the SCDO Laboratory Treasury on SCDO Shard0 (EVM).
2. **Idle mining:** the pool pays your address directly.
3. **Folding@home:** pays nothing until the SCDO rate is set. It is currently 0.

## Who do I contact?

Email admin@apeccapital.org.

For information only. Not financial advice. SCDO tokens have no promised market value. No promise of block reward or market value.
