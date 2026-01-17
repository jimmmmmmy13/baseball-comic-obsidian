# 命名與路徑規範：最常見原因（Day 2）

網站只會讀取以下路徑：

`data/students/<10碼英數字學號>/index.json`

---

## 1) 學號資料夾命名錯誤

正確：
- `A123456789`（10 碼英數）

錯誤（全部不行）：
- `A12345678`（少一碼）
- `A123456789-Name`（多符號）
- `王小明`（中文）
- `A123 456789`（空白）

---

## 2) 層級放錯

正確：
- `data/students/<學號>/index.json`

錯誤：
- `students/<學號>/index.json`
- `data/<學號>/index.json`
- `data/students/<學號>/vault/index.json`
