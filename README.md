# AI 分身起步包 — 建立一個會記得你、會跟你磨合的 AI 助理

> **第一次來的人：先看圖文版使用指南 → https://j6259676-bot.github.io/cc-starter-kit/**
> 這份 README 是同樣的內容，網頁版比較好讀，也方便直接傳給別人。

任何人都能用：老師、行政、自己接案、教會同事都一樣。不需要會寫程式，全程用中文對話完成。照著做，30 分鐘內你會有：

1. **一個認識你的 AI 助理**：知道你是誰、做什麼工作、說話習慣、哪些事要先問你
2. **一套看得見的記憶**：你糾正過的錯，它寫成檔案，下次不再犯；你隨時打得開檢查
3. **一套會自己長大的機制**：同樣的錯犯兩次，它主動提案升級成規則；同樣的事做三次，它主動提案變成固定流程

這個包最重要的不是「給你設定檔」，而是**讓你學會跟它一起工作** — 設定檔只是骨架，肉是你每天用的過程中長出來的。

---

## 快速開始（三步驟，不用開終端機）

### 第 1 步：安裝 Claude 桌面 App

到 [claude.com/download](https://claude.com/download) 下載 Claude 桌面 App，安裝後登入。需要付費方案（Pro 以上）才能用 Code 功能。

### 第 2 步：下載這個資料夾

在 GitHub 頁面點綠色 `Code` 按鈕 → `Download ZIP`（或直接點[這裡下載](https://github.com/j6259676-bot/cc-starter-kit/archive/refs/heads/main.zip)），解壓縮後把資料夾改名叫 `my-agent`，放到「文件」裡。

這個資料夾之後會存你的個人偏好和工作資料，是你自己的私人空間。

### 第 3 步：叫它帶你完成設定

1. 打開 Claude 桌面 App，切到上方的 **Code** 分頁
2. 選擇剛剛的 `my-agent` 資料夾開始新對話
3. 打這五個字，按 Enter：

> 帶我完成設定

它會照 [SETUP.md](SETUP.md) 一次問你一個問題（你是誰、最花時間的三件事、你希望它怎麼跟你確認事情），把答案寫進設定，最後**帶你做一件今天真的要做的事**。全程你只要回答問題，不用自己改任何檔案。

---

### 習慣用終端機的人

```bash
curl -fsSL https://claude.ai/install.sh | bash
```

```bash
cd ~/Documents/my-agent && claude
```

用 Codex 的人：包裡附了 `AGENTS.md`，它會指向 CLAUDE.md，其餘步驟一樣。想讓 Codex 直接讀 CLAUDE.md，在 `~/.codex/config.toml` 加一行 `project_doc_fallback_filenames = ["CLAUDE.md"]`。

## 這個資料夾裡有什麼

| 檔案／資料夾 | 用途 |
|---|---|
| `CLAUDE.md` | AI 助理的核心規則。每次開工都會自動讀 |
| `SETUP.md` | 初次設定的訪談腳本（給 AI 讀的） |
| `GROWTH.md` | **最重要的一份文件**：怎麼讓它越用越懂你 |
| `000_Agent/memory/` | 記憶：認識你、你的糾正、進行中的事、東西放在哪 |
| `100_Todo/` | 工作區：草稿、進行中專案、封存 |
| `200_Reference/writing-samples/` | 放你自己寫過的東西，讓它學你的語氣 |
| `modules/` | 選配模組（不裝也完全可以） |

## 選配模組

設定時它會依你的工作推薦，也可以之後對它說「幫我安裝 modules/某某模組」：

| 模組 | 適合誰 | 內容 |
|---|---|---|
| [modules/dev-workflow](modules/dev-workflow/) | 任何要做「大東西」的人 | 一整學期教材、一個報名頁、一個小工具的五步流程，不限程式 |
| [modules/data-tools](modules/data-tools/) | 常處理表單、報表、試算表的人 | Google 試算表整理、Apps Script 開發守則、前人踩坑精選 |
| [modules/the-hope](modules/the-hope/) | The Hope 同事（必裝） | 教會用語、教會帳號、會友個資規則 |
| [modules/pastoral](modules/pastoral/) | The Hope 牧養、小組、關懷 | 1on1 紀錄流程、會議紀錄整理、群發信踩坑 |
| [modules/design-media](modules/design-media/) | The Hope 設計、媒體、社群 | The Hope 設計系統、對外文案守則 |

## 卡住了？

先問它本人：「我想要 X，但你剛剛做成 Y，為什麼？我該怎麼調整設定？」它看得到自己的設定檔，通常能直接告訴你要改哪裡。這也是 [GROWTH.md](GROWTH.md) 教的第一課。
