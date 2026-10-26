# Lexi 背單字

一個全離線、資料只存在自己裝置上的英文單字網頁 App。

👉 線上使用：https://ellie-tai.github.io/lexi/

## 功能

- 每日打卡：新字、複習、產出、克漏字四關
- 額外練習：拼字聽寫、中→英回想、句子克漏字、易混淆字、翻卡整理
- 程度測驗：自動調整難度，估計 CEFR 程度
- 字表：可依等級篩選、搜尋，**按 💡 看字首字根拆解**（基礎／進階兩層、字源小故事、字根主題）
- 學習數據、深淺色、備份與還原

## 檔案

| 檔案 | 內容 |
|---|---|
| `index.html` | 網頁 App 本體（含單字資料） |
| `roots.json` | 字首字根拆解資料，網頁打開時在背景讀取 |

本機測試：因為瀏覽器不允許直接雙擊打開的網頁讀取其他檔案，請在資料夾內執行
`python -m http.server`，再打開 http://localhost:8000 。

## 資料來源與授權

- **字首字根資料（`roots.json`）**：由 Claude（Anthropic）協助產生，並以 MorphoLex-en 比對檢查。
  - MorphoLex-en：Sánchez-Gutiérrez, C.H., Mailhot, H., Deacon, S.H. et al. *Behavior Research Methods* (2017). https://github.com/hugomailhot/MorphoLex-en ，授權 CC BY-NC-SA 4.0。
  - 因此 `roots.json` 以 [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) 授權釋出，僅限非商業使用。
