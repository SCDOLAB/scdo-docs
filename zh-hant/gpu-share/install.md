# 安裝 GPU 算力共享程式

GPU 算力共享程式 1.2.4 讓閒置的 NVIDIA 顯示卡在電腦沒人用時自動運算。不需要錢包、不需要節點、不需要註冊：下載、解壓縮、雙擊即可。

**系統需求：** Windows 10／11 64 位元，NVIDIA 顯示卡（4GB 顯示記憶體以上）。

## 第一步：下載並核對檔案

1. 前往 https://scdoscan.io/gpu-share/?ref=gitbook ，下載 Windows 版壓縮檔 `scdo-gpu-share-worker-1.2.4-win-x64.zip`。
2. 執行任何程式之前，先核對檔案。在壓縮檔所在的資料夾開啟 PowerShell，輸入：

```powershell
Get-FileHash .\scdo-gpu-share-worker-1.2.4-win-x64.zip -Algorithm SHA256
```

結果必須完全等於：

```
96e19a186a53e42c59bd67c00244afff166acf03df1e80ba62a90cc55c8880f4
```

如果不相符，請刪除檔案，並只從 https://scdoscan.io/gpu-share/?ref=gitbook 重新下載。

## 第二步：解壓縮

把壓縮檔解到任意資料夾，例如 `C:\scdo-gpu-share\`。之後搬移資料夾或重新解壓縮都沒關係：金鑰另外存放，位址不會變。

## 第三步：雙擊執行

雙擊 `scdo-gpu-share-worker-1.2.4-win-x64.exe`。

如果 Windows 跳出「Windows 已保護您的電腦」：這個程式沒有程式碼簽章，所以可能出現這個提示。確認雜湊值相符後，按「其他資訊」，再按「仍要執行」。

這樣就完成了，程式不需要你輸入任何資料。第一次啟動時，它會自動建立你的工作機金鑰，以及 SCDO Shard0 (EVM) 上的 0x 收款位址。電腦空閒時會先挖 SCDO：官方礦工包內的 Rigel 用你的位址直接連上 SCDO 公開礦池。Rigel 為閉源軟體，收取 0.7% 開發者費用。若挖礦無法啟動，改由官方 Folding@home 用戶端接手，以 SCDO Laboratory 團隊（#1068523）參與醫學研究運算。

## 備份金鑰

{% hint style="warning" %}
程式第一次啟動時，會在 `%APPDATA%\SCDO\gpu-share` 建立 `worker.key`。這把私鑰對應的 0x 位址就是你的收款位址。

* 請立刻備份 `%APPDATA%\SCDO\gpu-share\worker.key`，例如存到離線保管的隨身碟。
* 絕對不要把這個檔案交給任何人。SCDO 實驗室絕不會向你索取。
* 誰拿到這個檔案，誰就能控制這個位址。
{% endhint %}

開啟這個資料夾的方法：按 **Win + R**，輸入 `%APPDATA%\SCDO\gpu-share`，再按 Enter。

## 重新安裝或搬移資料夾

金鑰存在 `%APPDATA%\SCDO\gpu-share`，不在程式資料夾裡。只要沒有刪除 `%APPDATA%\SCDO\gpu-share`，重新安裝、解壓縮到新資料夾或搬移資料夾，都還是同一臺工作機、同一個位址。


## 查詢你的工作機

在 https://scdoscan.io/gpu-share/?ref=gitbook#check 的查詢欄輸入你的工作機位址，或到 https://scdoscan.io 搜尋該位址，就能看到鏈上紀錄。

## 停止或移除

* **停止：** 關閉程式視窗，或在工作管理員結束 `scdo-gpu-share-worker-1.2.4-win-x64.exe`。程式不會安裝 Windows 服務。
* **移除：** 刪除解壓縮後的資料夾。要完全移除，請一併刪除 `%APPDATA%\SCDO\gpu-share`（若有 `%AppData%\scdo-gpu-worker` 也一起刪）。若之後可能再用，請先備份 `worker.key`。

其他問題請看[常見問題](faq.md)。

本文僅供參考，不構成財務建議。SCDO 代幣不承諾任何市場價值，也不承諾區塊獎勵。
