---
name: feedback-example
description: 格式範例 — 被糾正或踩到坑時這樣記
metadata:
  type: feedback
---

# Feedback 範例檔

> 真實的 feedback 檔照這個結構寫，檔名 `feedback_主題.md`，寫完在 MEMORY.md 的 Feedback 段加一行索引。
> 開頭 `---` 包起來的那幾行叫「標頭」，讓 AI 一眼知道這筆記憶是什麼、什麼時候用得到。

## 範例一：被糾正

```markdown
---
name: no-dear-in-parent-messages
description: 寫給家長的訊息開頭不用「親愛的」
metadata:
  type: feedback
---

- **錯誤做法**：家長群組公告開頭寫「親愛的家長們」
- **正確做法**：直接寫「各位家長好」
- **原因**：「親愛的」在這個群組顯得太客套，我的風格是直接、溫暖
- **日期**：2026-11-10
```

## 範例二：踩到坑

```markdown
---
name: sheet-date-off-by-one
description: Google 試算表的日期讀出來會差一天
metadata:
  type: feedback
---

- **情境**：從 Google 試算表讀日期欄位做統計
- **症狀**：讀出來的日期比表上顯示的早一天
- **原因**：讀到的是含時區的時間，轉文字時用錯時區
- **下次這樣做**：轉文字時明確指定台北時區（Asia/Taipei）
- **日期**：2026-11-10
```
