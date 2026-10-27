# Lexi 背單字

一個全離線、資料只存在自己裝置上的英文單字網頁 App。

👉 線上使用：https://ellie-tai.github.io/lexi/

## 功能

- 每日打卡：新字、複習、產出、克漏字四關
- 額外練習：拼字聽寫、中→英回想、句子克漏字、易混淆字、翻卡整理
- 9252 個單字：CEFR A1–C2，並完整收錄大考中心《高中英文參考詞彙表》（七千單）的實詞
- 兩套分級：CEFR 與大考中心 L1–L6 可同時勾選，單字卡顯示兩種標籤
- 程度測驗：自動調整難度，估計 CEFR 程度並建議對應的大考級別
- 字表：可依等級篩選、搜尋，**按 💡 看字首字根拆解**（基礎／進階兩層、字源小故事、字根主題）
- 用字根學單字：每天一個字根主題，一次學一組同字根的字，可記錄已學完的主題
- 學習數據、深淺色、備份與還原

## 檔案

| 檔案 | 內容 |
|---|---|
| `index.html` | 網頁 App 本體（含單字資料） |
| `roots.json` | 字首字根拆解資料，網頁打開時在背景讀取 |

本機測試：因為瀏覽器不允許直接雙擊打開的網頁讀取其他檔案，請在資料夾內執行
`python -m http.server`，再打開 http://localhost:8000 。

## 資料來源與授權

- **七千單字表**：大學入學考試中心《高中英文參考詞彙表》（111 學年度起適用），依其「僅供非營利目的使用，轉載請註明出處」之規定使用。
- **新增單字的音標**：取自 [ECDICT](https://github.com/skywind3000/ECDICT)（MIT License, Copyright (c) 2025 Linwei）。
- **等級說明**：多益對照依 ETS《Mapping the TOEIC Tests on the CEFR》；全民英檢對照依教育部公告英語能力檢定對照表。

- **字首字根資料（`roots.json`）**：由 Claude（Anthropic）協助產生，並以 MorphoLex-en 比對檢查。
  - MorphoLex-en：Sánchez-Gutiérrez, C.H., Mailhot, H., Deacon, S.H. et al. *Behavior Research Methods* (2017). https://github.com/hugomailhot/MorphoLex-en ，授權 CC BY-NC-SA 4.0。
  - 因此 `roots.json` 以 [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) 授權釋出，僅限非商業使用。
