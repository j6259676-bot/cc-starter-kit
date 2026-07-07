# DESIGN.md — The Hope 設計系統（精簡版）

> AI 做任何 The Hope 介面、網頁、圖卡前先讀這份。完整版與 Logo 檔案向線上分部索取後放 `200_Reference/design/`。

## 品牌核心

**YOU BELONG HERE.** — 大膽、溫暖、極度歡迎。
設計決策唯一標準：這個設計是否讓人感覺「我在這裡有位置」？

## 色票

| 用途 | Hex | 備註 |
|---|---|---|
| 主要強調色 / CTA | `#FFCC32` | Hope Yellow |
| 深色主背景 | `#1D292E` | Deep Blue |
| 次要深色 | `#3C5464` | Midnight Blue |
| 暖色中間調 | `#C8956A` | Sand |
| 淡暖色背景 | `#EDE0D4` | Cream |
| 頁面底色 | `#F6F0EA` | Cream Light |
| 純黑 | `#0D1618` | Black |

## 常用配色組合

| 場景 | 背景 | 主文字 | 強調 |
|---|---|---|---|
| 深色 hero / nav | `#1D292E` | `#FFFFFF` / `#EDE0D4` | `#FFCC32` |
| 暖色 section | `#EDE0D4` | `#1D292E` | `#C8956A` |
| 黃色 CTA banner | `#FFCC32` | `#1D292E` | — |
| 白色 card | `#FFFFFF` | `#1D292E` | `#FFCC32` |

## 字體

```css
/* 英文標題與內文（官方 Gotham 的免費替代） */
font-family: 'Montserrat', sans-serif;
/* 繁體中文 */
font-family: 'Noto Sans TC', 'PingFang TC', 'Microsoft JhengHei', sans-serif;
```

中文大標用 Noto Sans TC 粗黑（weight 700-900），不用手寫或藝術字體（中文會糊、難讀）。

## 圖示

- 一律 [Lucide Icons](https://lucide.dev)，`stroke-width: 2`
- **不用 emoji** — 任何介面、文宣、正式文件都不用

## 用語地雷

- 口號是 `YOU BELONG HERE`（不是 THEY）
- 對外一律「服事夥伴」（不是「同工」）
- 「牧養」（不是「物養」）
