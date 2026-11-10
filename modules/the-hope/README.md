# the-hope — The Hope 同事必裝

給在 The Hope 服事或工作的夥伴。起步包核心是通用版（任何人都能用），教會專屬的用語、帳號與個資規則都收在這個模組。

**The Hope 同事請先裝這個**，再依角色加裝 `pastoral`、`design-media`。

裝完你會多：

1. **教會用語守門**：牧養、服事夥伴、YOU BELONG HERE 這些絕不能寫錯的字
2. **帳號判斷**：私人 Gmail 和 `@thehope.co` 教會帳號分清楚
3. **會友個資規則**：會友名單、關懷紀錄只在教會系統與本機之間流動

## 安裝步驟（Claude 照做）

1. 把 [CLAUDE-snippet.md](CLAUDE-snippet.md) 的內容合併進使用者 CLAUDE.md 的 §1（先給使用者看過再改）
2. 問使用者：「你的教會帳號是哪一個？私人 Gmail 是哪一個？」寫進 `000_Agent/memory/reference_accounts.md`（只寫帳號名稱，不寫密碼），並在 MEMORY.md 的 Reference 段加索引
3. 問使用者負責哪個分部、哪些事工，補進 CLAUDE.md §5「關於我」

## 為什麼這些規則要獨立成模組

起步包也會給教會以外的人用（家人、朋友）。把教會用語放在核心，會讓他們的 AI 莫名其妙去糾正「同工」這種他們根本不會用到的字。
