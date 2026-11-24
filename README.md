# 棗紅公館｜公館紅棗風土與農遊

以原生 HTML、CSS 與 JavaScript 製作的響應式互動網站，使用 Node.js 內建 HTTP server，無需外部套件或建置步驟。

## 本機啟動

需求：Node.js 18 或更新版本。

```bash
npm install
npm run build
npm start
```

這個輕量專案不需要編譯；`npm run build` 保留為部署平台相容的空操作。啟動後開啟 `http://localhost:3000`。

## Render 部署

建立 **Web Service**，連結此 Git 儲存庫並設定：

- Build Command：`npm install && npm run build`
- Start Command：`npm start`
- Environment：`Node`
- Instance Type：可依流量選擇

伺服器會監聽 Render 提供的 `PORT` 環境變數與 `0.0.0.0`。

## 分析追蹤

複製 `.env.example` 作為設定參考，在本機或 Render 設定 `GA4_ID`、`GTM_ID`。瀏覽器端亦可從網址參數 `?ga4=G-...&gtm=GTM-...` 覆寫，以支援純靜態託管情境。追蹤封裝會送出 `select_content`、`add_to_cart`、`begin_checkout`、`booking_submit`、`quiz_complete`、`recommendation_select`、`recipe_calculate` 等事件；沒有設定 ID 時不載入追蹤腳本。

## 功能

- 品牌首頁、產地故事、品質辨識、農遊預約、商品商城、交通與 FAQ。
- 三題產地辨識測驗、使用情境商品推薦、紅棗食譜計算器、農遊行程規劃器。
- 常溫及冷藏購物車、數量增減、快速結帳表單與模擬物流狀態。無真實金流、訂單或預約 API。
- 手機版導覽、RWD 版面、SEO metadata、JSON-LD、GA4 / GTM 事件封裝。

商品價格、庫存、預約及折價碼為互動展示用的模擬資料，正式營運前請依農會與果園資訊更新。

