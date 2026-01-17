# 匯出失敗：export.py / Python 排除（Day 2）

---

## 1) 雙擊 run_export.bat 沒反應或閃一下就關掉

請改用以下方式執行（看得到錯誤）：

### Windows
1. 在你的學號資料夾中（有 export.py 的那層）
2. 右鍵空白處 →「在終端機中開啟」或「Open in Terminal」
3. 輸入：

python export.py


把畫面上的錯誤訊息截圖給老師。

---

## 2) 出現 `python is not recognized...`（Windows 最常見）

表示 Python 沒安裝或沒加入 PATH。

### 自救檢查
1. 開終端機輸入：

python --version

2. 若不行，再試：

py --version


若 `py` 可以用，請改用：
- `run_export.bat` 內的 python 改成 `py`（或請老師協助）

---

## 3) 出現 `找不到 vault/ 資料夾`

表示你的資料夾結構不正確。

你應該在：
- `data/students/<學號>/vault/` 看到你的筆記檔

而 `export.py` 必須跟 `vault/` 同一層。

---

## 4) 產生了 index.json，但網站查不到資料

常見原因：
- 你把筆記放在 vault 根目錄，但 export.py 期待子資料夾（players/events/glossary）
- 解法：
- 依課程規範把檔案放進 `vault/players/`, `vault/events/`, `vault/glossary/`
- 再重新執行匯出
