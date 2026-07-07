# GAS-PITFALLS — Apps Script 踩坑精選

> The Hope 夥伴開發 GAS 工具累積的坑。AI 開發任何 GAS 專案前先讀這份。每一條都是真實摔過的。

## 部署與授權

1. **`clasp push` 不等於上線。** push 只更新程式碼（HEAD），網頁用的 `/exec` 網址還是舊版。要另外執行部署（更新既有 deployment，不是新建），用 `clasp deployments` 核對版本。這是最常見的「我明明改了怎麼沒變」。

2. **加了新的 Google 服務（Gmail、Drive、Calendar…）後，部署不會自動要求授權。** 需要在 GAS 網頁編輯器裡手動執行一次任何函式，跳出 OAuth 視窗完成授權，網頁版才會動。

3. **改了 Script Property 設定值卻沒生效** — GAS 的執行個體會快取檔案頂層讀進來的設定。解法：把設定改成在 `doGet`/函式內讀取，或重新部署強制刷新。

4. **專案裡不能有兩個 `doGet`。** 多檔案專案若兩個檔案都定義了 `doGet`，後面的會蓋掉前面的，網頁直接壞掉（常見症狀：401 或空白頁）。合併成一個。

## 資料與日期

5. **`getValues()` 讀日期欄位回傳的是 Date 物件不是字串**，直接轉字串會因時區差一天。手動用 `getFullYear/getMonth/getDate` 組字串，且 `getMonth()` 從 0 開始（一月是 0）。

6. **`A2:A` 這種範圍不會自動涵蓋 `appendRow` 新增的列**（若範圍是在舊資料上設定的）。資料驗證與格式保護要用整欄或程式動態設定。

7. **openById 開試算表需要完整的讀寫權限 scope**，即使你只是要讀。只讀需求可改用 Sheets 進階服務的 readonly scope，避免重新授權整包。

## 網頁前端

8. **`google.script.run` 不能巢狀呼叫** — 在 success handler 裡再呼叫一次會靜默失敗（沒有錯誤訊息）。解法：後端寫一個 wrapper 函式把兩件事做完，前端只呼叫一次。

9. **中文輸入法與即時重繪衝突** — 搜尋框 `oninput` 直接重繪整個區塊會把注音組字打斷。解法：搜尋結果放獨立的 div，輸入框節點永遠不動。

10. **onclick 屬性裡塞 JSON 會靜默失效** — `JSON.stringify` 的雙引號會截斷 HTML 屬性。要先把 `"` 換成 `&quot;`，或改用 addEventListener。

## 測試

11. **用 curl 測 GAS API：加 `-sL` 跟隨轉址**（GAS 回應一定先 302），但**不要加 `--post302`**（會拿到 404 HTML）。

12. **剛寫入的資料馬上重讀可能看到舊值**（快取延遲）。驗證寫入成功要等幾秒或改查來源 API，不要立刻比對總筆數。
