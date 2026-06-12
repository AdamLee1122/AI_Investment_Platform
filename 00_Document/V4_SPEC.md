# V4_SPEC.md

Version: V4
Last Update: 2026-06-13

---

# V4 目標

建立台股 + 美股 AI 投資研究平台。

提供：

- 股票池管理
- 技術指標分析
- AI評分
- 類股分析
- 風險指標
- Telegram推播
- 每日自動化執行

---

# V4 功能需求

## 股票資料

[x] 台股股票池

目標：

- 台股1980+

資料來源：

- Yahoo Finance

---

[x] 美股股票池

目標：

- 美股3000+

資料來源：

- Yahoo Finance

---

## 技術分析

[x] MA20
[x] MA60
[x] RSI
[x] MACD

---

## AI評分系統

目前：

- 技術面評分

未來：

- 類股評分
- 總經評分
- 情緒評分

---

## 類股分析

開發中：

[ ] AI晶片
[ ] 半導體
[ ] IC設計
[ ] AI伺服器
[ ] 記憶體
[ ] 光通訊
[ ] 機器人
[ ] ETF

目標：

每個類股產生：

- Top10
- Top20

排行榜

---

## 永久保留池

開發中

用途：

長期追蹤核心標的

例如：

- 2330.TW
- 2454.TW
- NVDA
- MSFT
- GOOGL

---

## 風險指標

開發中

[ ] NFP
[ ] Unemployment
[ ] Fed Rate

輸出：

- Low Risk
- Medium Risk
- High Risk

---

## 通知系統

已完成

[x] Telegram Bot

功能：

- /daily
- /watchlist
- /report

---

## 自動化

已完成

[x] run_daily.py

流程：

reset_db.py
↓
view_indicators.py
↓
build_selected_pool.py
↓
export_daily_report.py

---

# 資料庫架構

## stock_master

股票主檔

---

## indicators

技術指標

包含：

- MA20
- MA60
- RSI
- MACD
- AI Score

---

## watchlist_master

自選群組

目前：

- 我的最愛
- 自選股1
- 自選股2
- 自選股3
- 自選股4

---

## watchlist_stocks

群組成員

目前：

我的最愛
├─ 2330.TW
└─ 2454.TW

自選股1
└─ 2317.TW

自選股2
└─ 2308.TW

---

## sector_master

規劃中

用途：

類股管理

例如：

- AI晶片
- 半導體
- IC設計
- AI伺服器

---

# V4 完成標準

[ ] 類股 Top10
[ ] 永久保留池
[ ] NFP風險指標
[ ] 失業率風險指標
[ ] Fed風險指標
[ ] Telegram投資摘要
[ ] 每日自動執行

---

# V4 結案條件

當以下全部完成：

- 類股分析
- 永久保留池
- 總經風險分析
- Telegram推播

V4 正式結案。

進入 V5。
