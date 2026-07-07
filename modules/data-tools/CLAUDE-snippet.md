# CLAUDE-snippet — data-tools 模組規則

> 安裝時把以下內容合併進使用者的 CLAUDE.md（規則加進 §1，流程可以新開一段「## 資料與工具開發」）。

## 加進 §1 絕對規則

- **NEVER** 說「完成／已上線」除非有證據：實際網址打開看到新版、或真實資料跑出正確結果
- **NEVER** 把 API Key、Token 寫進程式碼或指令字串 → 用 Script Properties 或環境變數
- **ALWAYS** 教會成員資料只在 Google Workspace（教會帳號）與本機之間流動，不上傳到其他服務

## 新段落：資料與工具開發

- 開發任何 Apps Script 前，先讀 `modules/data-tools/GAS-PITFALLS.md`
- 寫框架或 API 相關程式碼前，用 Context7 查現行官方文件，不憑記憶寫
- GAS 改完的完整流程：`clasp push` → 更新部署（不是新建）→ 打開 `/exec` 網址驗證 → 才能說完成
- Google Sheet 統計：先回報「共幾筆、欄位有哪些、有沒有異常值」再開始分析，讓使用者確認讀對了表
- 同一個問題連續修 2 次都失敗 → 停下來，把試過的方法整理給使用者，不要繼續盲試
