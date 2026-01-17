# Day 2 Debug 單頁速查表（請先看這一頁）

本頁是「最快自救指南」。
遇到問題時，請先對照下面的症狀 → 解法。
90% 的問題可以在這一頁解決。

--------------------------------------------------

一、GitHub Desktop / Commit / PR

Q1：我 Commit 做錯了，但「還沒 Push」
症狀：
- Commit 完才發現檔案不對
- 還沒按 Push origin

解法（最安全）：
1. GitHub Desktop → History
2. 找到你想回到的正確 commit
3. Branch → Reset to this commit
4. 選 Mixed
5. 修正檔案 → 重新 Commit

--------------------------------------------------

Q2：我 Commit 做錯了，而且「已經 Push」
症狀：
- 已 Push 到自己的 branch
- PR 還沒合併

解法（請用 Revert）：
1. GitHub Desktop → History
2. 右鍵做錯的 commit
3. Revert this commit
4. Push origin

不要用 Reset，避免 PR 混亂。

--------------------------------------------------

Q3：我已經開 PR，但內容錯了
解法：
- 不要開新 PR
- 在同一個 branch 修正
- Commit + Push
- PR 會自動更新

--------------------------------------------------

Q4：我不知道現在在哪個 branch
檢查：
- GitHub Desktop 上方的 Current branch
- 正確應該是：data-你的學號
如果你在 main，請立刻切回自己的 branch。

--------------------------------------------------

二、export / Python / index.json

Q5：雙擊 run_export.bat 沒反應或閃退
解法：
1. 在你的學號資料夾中
2. 右鍵 → 在終端機中開啟
3. 輸入：python export.py
4. 截圖錯誤訊息

--------------------------------------------------

Q6：出現 python is not recognized
原因：
- Python 沒安裝或沒加到 PATH

自救檢查：
python --version
或
py --version

--------------------------------------------------

Q7：出現找不到 vault 資料夾
原因：
- export.py 與 vault 不在同一層

正確結構：
你的學號/
- export.py
- run_export.bat
- index.json
- vault/

--------------------------------------------------

三、Obsidian vault 問題

Q8：我不知道原本 vault 在哪
解法：
- Obsidian → Open folder as vault
- 或搜尋你筆記中獨特的檔名

--------------------------------------------------

Q9：我搬移 vault 後 Obsidian 打不開
解法：
- 不要點舊 vault
- Open folder as vault
- 指到 data/students/你的學號/vault/

--------------------------------------------------

四、網站抓不到資料

Q10：PR 合併了但網站沒有我
請檢查：
1. PR 是否已合併到 main
2. 是否有 index.json
3. 路徑是否正確：
data/students/10碼學號/index.json

--------------------------------------------------

五、三句口訣（請背）

還沒 Push → Reset
已經 Push → Revert
已經 PR → 修正再 Commit

--------------------------------------------------

舉手前請先：
1. 看完本頁
2. 截圖錯誤畫面
3. 確認在 data-你的學號 branch
