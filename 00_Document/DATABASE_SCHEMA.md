# DATABASE_SCHEMA

最後更新：
2026-06-13

資料庫：

database/stock.db

---

# stock_master

股票主檔

用途：

保存所有可分析股票

欄位：

id
symbol
stock_name
market
sector
keep_flag

範例：

2330.TW
台積電
TW
半導體

NVDA
NVIDIA
US
AI晶片

---

# indicators

技術指標

用途：

每日分析結果

欄位：

id
symbol
date
ma20
ma60
rsi
macd
score

範例：

2330.TW
2026-06-13
2290.44
2115.54
50.11
33.29
100

---

# selected_pool

AI推薦池

用途：

保存每日推薦股票

預計欄位：

id
symbol
score
rank
date

---

# keep_pool

永久保留池

用途：

長期持有股票

預計欄位：

id
symbol
note

---

# watchlist_master

自選群組

用途：

管理群組名稱

範例：

我的最愛
自選股1
自選股2
自選股3
自選股4

---

# watchlist_stocks

群組股票

用途：

群組與股票關聯

範例：

我的最愛
2330.TW

我的最愛
2454.TW

自選股1
2317.TW

---

# Future Tables

V4

sector_master

macro_risk

---

V5

daily_price

financial_data

news_data

macro_data

---

V6

research_report

ai_summary

---

V7

youtube_transcript

news_sentiment

strategy_history
