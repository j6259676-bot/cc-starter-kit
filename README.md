# Claude Code 起步包 — 建立你的 AI 分身

這是給 The Hope 夥伴的 Claude Code 起始套件。照著做，30 分鐘內你會有：

1. 一個認識你的 AI 分身（知道你是誰、負責什麼事工、說話習慣）
2. 一套會越用越聰明的記憶系統（你糾正過的錯，它不會再犯）
3. 依你的角色選配的工具模組（牧養、設計媒體、資料工具）

這個包最重要的目的不是「給你設定檔」，而是**讓你學會自己養這個 AI 分身**。設定檔只是骨架，肉是你每天用的過程中長出來的。

---

## 快速開始（三步驟）

### 第 1 步：安裝 Claude Code

打開「終端機」（Terminal，Mac 內建，用 Spotlight 搜尋就有），貼上：

```bash
curl -fsSL https://claude.ai/install.sh | bash
```

裝好後輸入 `claude`，會引導你登入。你需要 Claude Pro 或 Max 訂閱（或公司提供的帳號）。

### 第 2 步：下載這個資料夾

**方法 A（不會 git 也沒關係）**：在 GitHub 頁面點綠色 `Code` 按鈕 → `Download ZIP` → 解壓縮到你想放的位置（建議 `~/Documents/my-agent`）。

**方法 B（會用 git）**：

```bash
git clone <這個 repo 的網址> ~/Documents/my-agent
cd ~/Documents/my-agent
rm -rf .git   # 斷開跟模板的連結，這個資料夾之後是你的私人空間
```

注意：這個資料夾之後會存你的個人偏好與事工資料，**不要**把它推回共用的模板 repo。

### 第 3 步：讓 Claude 帶你完成設定

```bash
cd ~/Documents/my-agent
claude
```

然後對它說：

> 帶我完成設定

Claude 會照 [SETUP.md](SETUP.md) 一步步問你問題、寫好你的個人設定、推薦適合你角色的模組。全程不用自己改任何檔案。

---

## 這個資料夾裡有什麼

| 檔案／資料夾 | 用途 |
|---|---|
| `CLAUDE.md` | AI 分身的核心規則。每次開啟 Claude Code 都會自動讀取 |
| `SETUP.md` | 初次設定的引導腳本（給 Claude 讀的） |
| `GROWTH.md` | **最重要的一份文件**：怎麼讓 AI 分身越用越聰明 |
| `000_Agent/memory/` | 記憶系統：偏好、踩過的坑、專案脈絡 |
| `100_Todo/` | 工作區：草稿、進行中專案、封存 |
| `200_Reference/writing-samples/` | 放你自己的寫作範例，AI 學你的語氣 |
| `modules/` | 選配模組：牧養、設計媒體、資料工具 |

## 選配模組

設定完成後，依你的角色安裝（對 Claude 說「幫我安裝 modules/某某模組」即可）：

| 模組 | 適合誰 | 內容 |
|---|---|---|
| [modules/pastoral](modules/pastoral/) | 牧養、小組、關懷 | Notion 任務系統、1on1 紀錄流程、會議紀錄整理、群發信踩坑 |
| [modules/design-media](modules/design-media/) | 設計、媒體、社群 | The Hope 設計系統（色票、字體、圖示規則）、文案語氣守則 |
| [modules/data-tools](modules/data-tools/) | 資料、表單、工具開發 | Google Sheet 整理、Apps Script 開發流程、前人踩坑精選 |
| [modules/dev-workflow](modules/dev-workflow/) | 任何要做「大東西」的人 | 做一個報名頁、一份完整教材、一個小工具時的五步流程，不限程式 |

## 卡住了？

先問 Claude 本人：「我想要 X，但你剛剛做成 Y，為什麼？我該怎麼調整設定？」——它看得到自己的設定檔，通常能直接告訴你要改哪裡。這也是 [GROWTH.md](GROWTH.md) 教的第一課。
