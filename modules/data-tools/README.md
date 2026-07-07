# data-tools — 資料／工具開發模組

給處理資料表、問卷統計、或想做小工具（Google Apps Script 等）的夥伴。裝完你會有：

1. **Google Sheet 整理流程**：貼一個 Sheet 連結，AI 幫你統計、找異常、產摘要
2. **Apps Script（GAS）開發守則**：用 clasp 讓 AI 直接讀寫你的 GAS 專案，不用複製貼上
3. **前人踩坑精選**：The Hope 夥伴開發 GAS 工具兩年累積的坑，直接繼承，不用重摔

## 安裝步驟（Claude 照做）

### 1. 合併規則

把 [CLAUDE-snippet.md](CLAUDE-snippet.md) 的內容加進使用者 CLAUDE.md（先給使用者看過再改）。

### 2. 連接 Context7（查官方文件用）

```bash
claude mcp add --transport http context7 https://mcp.context7.com/mcp
```

作用：AI 寫框架程式碼前先查現行官方文件，而不是憑記憶寫出過時語法。

### 3. 若使用者要開發 GAS：安裝 clasp

```bash
npm install -g @google/clasp
clasp login
```

登入時注意用**教會帳號**授權（如果工具是教會專案）。

### 4. 繼承踩坑記憶

把 [GAS-PITFALLS.md](GAS-PITFALLS.md) 留在原位即可 — CLAUDE-snippet 已要求 AI 開發 GAS 前先讀它。

### 5. 帶跑一次流程

請使用者提供一份真實的 Google Sheet（問卷結果、名單、報名表），做一次「讀取 → 統計 → 摘要」，示範資料流程。

## 日常用法

- 「幫我統計這份問卷」＋ Sheet 連結 → 結構化統計摘要
- 「幫我改這個 Apps Script」 → clasp pull → AI 修改 → 測試 → clasp push → **另外執行部署**（這是最常摔的坑，見 GAS-PITFALLS 第 1 條）
- 「這份名單有沒有重複或異常？」 → 資料品質檢查

## 心法

工具開發最大的坑不是寫程式，是「以為完成了但沒有」。守則：說「完成」之前，一定要有證據 — 打開實際網址看到新版本、跑一次真實資料看到正確結果。AI 說改好了不算數，看到才算數。
