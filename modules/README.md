# modules/ — 選配模組

依你的角色安裝需要的，不用全裝。**安裝方式：對 Claude 說「幫我安裝 modules/模組名」**，它會照該模組的 README 執行：把 `CLAUDE-snippet.md` 的規則合併進你的 CLAUDE.md、完成需要的工具連接、帶你跑一次流程。

| 模組 | 適合誰 | 裝了會多什麼 |
|---|---|---|
| [pastoral](pastoral/) | 牧養、小組、關懷 | Notion 任務與 1on1 紀錄流程、會議紀錄整理、牧養用語規則、群發信踩坑 |
| [design-media](design-media/) | 設計、媒體、社群 | The Hope 設計系統（色票、字體、圖示）、對外文案守則 |
| [data-tools](data-tools/) | 資料、表單、工具開發 | Google Sheet 整理流程、Apps Script 開發守則、前人踩坑精選 |
| [dev-workflow](dev-workflow/) | 任何要做「大東西」的人 | 五步流程（拷問→規格→切片→實作→檢查）＋五個指令，不限程式 |

## 每個模組的結構

```
模組名/
├── README.md            ← 安裝步驟與使用說明（人和 Claude 都要讀）
├── CLAUDE-snippet.md    ← 要合併進 CLAUDE.md 的規則段落
└── （其他參考檔案）
```

## 之後想自己加模組？

模組沒有魔法 — 就是「一段規則 + 一些參考檔案」。當你在某個領域累積了足夠的 feedback 記憶，跟 Claude 說「把這個領域的記憶整理成一個模組」，你就有了可以分享給其他夥伴的模組。做出好用的，歡迎貢獻回這個起步包。
