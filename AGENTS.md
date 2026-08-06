# AGENTS.md

這個資料夾的完整規則寫在 **[CLAUDE.md](CLAUDE.md)**，請先完整讀過再開始工作，並全程遵守，包括：

- §0 初次設定檢查（`000_Agent/memory/MEMORY.md` 第一行是 `SETUP:PENDING` 就照 [SETUP.md](SETUP.md) 帶使用者完成設定）
- §1 絕對規則與協作紀律（說「完成」前要有證據）
- §2 記憶系統（每個 session 開始讀 MEMORY.md，結束寫 daily）
- §4 資料路由（東西該寫去哪個資料夾）

> 為什麼有兩個檔案：Claude Code 讀 `CLAUDE.md`，Codex 讀 `AGENTS.md`。這份只是指路，規則不重複維護，一律以 CLAUDE.md 為準。
>
> 如果你偏好讓 Codex 直接讀 CLAUDE.md，在 `~/.codex/config.toml` 加上
> `project_doc_fallback_filenames = ["CLAUDE.md"]` 也可以，那樣就不需要這個檔案。
