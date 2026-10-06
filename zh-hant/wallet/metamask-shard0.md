# 把 SCDO Shard0 (EVM) 加入 MetaMask

SCDO Shard0 (EVM) 是相容 EVM 的工作量證明網路，鏈 ID 為 5680。只要正確填入網路資料，MetaMask 就能連上。請只使用本頁列出的數值，連線前先確認網域，也絕不要洩露私鑰或助記詞。

## 開始之前

請只從官方網站 https://metamask.io/ 安裝 MetaMask。不要從彈出視窗、陌生訊息或仿冒網站安裝錢包擴充功能。假的擴充功能可能竊取你的密碼或助記詞。

## 方法一：一鍵新增

1. 自己輸入網址或用書籤開啟 https://scdoscan.io/start.html 。
2. 點選「一鍵新增 SCDO Shard0 (EVM) 到 MetaMask」。
3. 在 MetaMask 中檢查請求內容並確認。MetaMask 會切換到 SCDO Shard0 (EVM)。

使用 MetaMask 手機應用程式時，請在應用程式內建的瀏覽器開啟 https://scdoscan.io/start.html ，再點選同一個按鈕。

## 方法二：手動新增

開啟 MetaMask 的網路選單，進入新增自訂網路的表單。不同版本的選單名稱略有不同，例如「設定」→「網路」→「新增網路」→「手動新增網路」。目標是開啟自訂網路表單，而不是選擇來路不明的建議網路。

逐項準確填入：

| 欄位 | 數值 |
| --- | --- |
| 網路名稱 | `SCDO Shard0 (EVM)` |
| RPC 網址 | `https://scdoscan.io/rpc/0` |
| 鏈 ID | `5680` |
| 貨幣符號 | `SCDO` |
| 區塊瀏覽器網址 | `https://scdoscan.io` |

* **RPC 網址：** 確認開頭是 `https`、網域正是 `scdoscan.io`、結尾是 `/0`。不要使用從留言、私訊或廣告複製來的網址。
* **鏈 ID：** `5680`（十六進位為 `0x1630`），不要多打空格或數字。
* **區塊瀏覽器網址：** `https://scdoscan.io`，不要附加追蹤參數，也不要用長得很像的網域。

儲存前把五個欄位再讀一遍，然後按「儲存」，並在網路選單切換到 SCDO Shard0 (EVM)。

新增網路絕不需要助記詞或私鑰。不要因為剛新增了網路，就確認任何意料之外的連線或簽名請求。

## Shard0 位址與 Classic 位址

SCDO Shard0 (EVM) 帳戶使用以 `0x` 開頭的標準 EVM 位址，和你在其他 EVM 網路上的位址相同。

SCDO Shard1 (Classic) 到 SCDO Shard4 (Classic) 使用 `1S01...`、`2S02...` 這類 Classic 位址，小數位數為 8 位。Classic 位址無法在 MetaMask 中使用，請改用 SCDO 網頁錢包 https://scdoscan.io/wallet/ 或[桌面版 SCDO 錢包](https://scdoscan.io/downloads/wallet/)。

## 在區塊瀏覽器上確認

開啟新分頁，自己輸入 https://scdoscan.io 。確認網址列正是 `scdoscan.io`，而且使用 HTTPS 連線。把你的 `0x` 位址貼到搜尋欄，就能看到它在 SCDO Shard0 (EVM) 上的餘額與紀錄。

請留意假的 RPC 網址、仿冒網站與意料之外的簽名請求。任何正當的設定教學都不需要你的私鑰或助記詞。

## 最後檢查

* MetaMask 從 https://metamask.io/ 安裝。
* 網路是 SCDO Shard0 (EVM)。
* RPC 網址是 https://scdoscan.io/rpc/0 。
* 鏈 ID 是 5680。
* 貨幣符號是 SCDO，區塊瀏覽器是 https://scdoscan.io 。
* 你的助記詞與私鑰只有你自己知道。

以上是網路連線說明。SCDO 代幣不承諾任何市場價值，也不承諾區塊獎勵。
