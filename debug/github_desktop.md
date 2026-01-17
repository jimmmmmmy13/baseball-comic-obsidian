# GitHub Desktop 常見問題與處理（Day 2）

本文件只使用 GitHub Desktop 的操作，不使用 git 指令。

---

## 1) 我 Commit 做錯了（但還沒 Push）

情境：你已經 Commit，但還沒按 Push origin。

### 方案 A：最簡單（建議）
1. 在 GitHub Desktop 上方選單：**Branch → Reset to this commit...**
2. 在 History 裡找到「你想回到的那個正確 commit」
3. 右鍵該 commit（或點選後操作 Reset）
4. Reset mode 選：
   - **Mixed**（最常用）：回到該 commit，但保留檔案變更在 Changes（你可再修改後重新 commit）
   - **Hard**（危險）：直接丟掉後面所有變更（除非你很確定）

> 教學建議：同學一律先用 Mixed。

---

## 2) 我 Commit 做錯了（而且已經 Push 了）

情境：你已經 Push 到自己的分支（例如 data-A123456789），但還沒開 PR 或 PR 還沒被合併。

### 方案 A：用「Revert」產生一個修正 commit（最安全）
1. GitHub Desktop → **History**
2. 找到做錯的那個 commit
3. 右鍵 → **Revert this commit**
4. 會自動產生一個「反向修正」的 commit
5. Push origin

這個方式的好處是：不會改寫歷史（避免衝突），老師也容易看懂。

### 方案 B：Reset（只建議老師或熟手）
- Reset 會改寫分支歷史，可能造成 PR 混亂。
- 除非老師要求，否則同學不要使用。

---

## 3) 我已經開 PR，但發現內容錯了

### 最簡單處理方式：在同一個分支繼續修
1. 不要開新分支
2. 直接修正檔案（路徑/內容）
3. Commit
4. Push
PR 會自動更新成最新內容。

---

## 4) 我 Push 失敗（常見原因）

### 可能原因 A：你還沒登入 GitHub Desktop
- GitHub Desktop → Preferences/Options → Accounts
- 登入你的 GitHub 帳號

### 可能原因 B：權限不足
- 你沒有被加入這個 repo 的 Collaborator
- 請舉手讓老師加入（或用 fork 流程）

---

## 5) 我不小心改到別人的資料夾或系統檔案

### 建議作法
1. 在 Changes 裡把不該改的檔案右鍵 → Discard changes
2. 確認你只改了：
   - `data/students/<你的學號>/...`

---

## 6) 我搞不清楚目前在哪個 branch

在 GitHub Desktop 上方看：
- Current branch 應該要是：`data-你的學號`

如果你在 main：
- 請先切回自己的 branch 再做事
