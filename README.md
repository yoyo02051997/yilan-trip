# 礁溪溫泉兩天一夜 · 行程頁

2026/06/20–21 礁溪兩天一夜的單檔行程頁，手機優先、可離線開啟、可直接部署到 GitHub Pages。

## 預覽

開啟 `index.html` 即可。

## 部署到 GitHub Pages

1. 在 GitHub 建立 repo `yilan-trip`，把這個資料夾推上去（`main` 分支）。
2. Repo → **Settings** → **Pages** → Source 選 `Deploy from a branch` → Branch 選 `main` / `/ (root)` → Save。
3. 等 1–2 分鐘後在 `https://<你的帳號>.github.io/yilan-trip/` 看到頁面。

## 修改行程

所有時間、地點、備註都集中在 `index.html` 檔頭的 `const TRIP = {...}` 物件，改那裡就好，內容與畫面分離。

- `meta`：標題、日期、住宿
- `days[].items[]`：每個行程點
  - `time` 時間（字串）
  - `name` 地點名
  - `cat` 類別：`move` / `food` / `sight` / `spring`（決定配色）
  - `catLabel` 類別小標籤
  - `icon` emoji 圖示
  - `note` 備註
  - `stay` 建議停留（可留 `null`）
  - `mapQuery` Google Maps 搜尋關鍵字（建議寫「店名 + 鄉鎮 + 縣市」精準度較高，留 `null` 則不顯示按鈕）
- `transport`、`tips`：底部兩個區塊的條列

## 規格摘要

- 單檔 `index.html`、無建置流程、無外部 JS
- Google Fonts：Fraunces / Noto Serif TC / Noto Sans TC
- 配色：蘭陽綠（jade）+ 溫泉琥珀（amber）+ 泉水青（spring）
- 類別配色：交通 jade-deep · 餐飲 amber · 景點 jade · 泡湯 spring
- 不使用 `localStorage` / `sessionStorage`
- `prefers-reduced-motion` 時關閉蒸氣動畫
- 鍵盤 focus 可見、Day 切換支援左右方向鍵

## 行程概覽

- **Day 1（6/20 週六）** 抵達羅東 → 麵線龜 → 國立傳藝中心 → 羅東夜市 → 礁溪悠宅
- **Day 2（6/21 週日）** 悠宅岩盤浴 + 按摩 → 樂山溫泉拉麵 → 五峰旗瀑布 → 湯圍溝 → 柯氏蔥油餅 → 19:58 返北
