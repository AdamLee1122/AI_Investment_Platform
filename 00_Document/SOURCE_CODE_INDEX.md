# SOURCE_CODE_INDEX

最後更新：
2026-06-13

版本：
V4

---

# 專案目的

本文件記錄所有 Python 程式用途。

避免：

- 重複建立程式
- 功能重疊
- AI 誤判架構

未來新增程式時必須同步更新本文件。

---

# 核心流程

run_daily.py

↓

reset_db.py

↓

view_indicators.py

↓

build_selected_pool.py

↓

export_daily_report.py

↓

Telegram / Email

---

# Database

init_db.py

用途：
建立 SQLite 資料庫

---

upgrade_db_v4.py

用途：
升級資料庫結構

---

# Stock Master

create_stock_master.py

用途：
建立 stock_master

---

seed_stock_master.py

用途：
匯入股票主檔

---

check_stock_master.py

用途：
檢查 stock_master

---

# Sector

create_sector_master.py

用途：
建立 sector_master

---

seed_sector_master.py

用途：
匯入產業分類

---

show_sector.py

用途：
顯示類股資料

---

# Keep Pool

create_keep_pool.py

用途：
建立永久保留池

---

seed_keep_pool.py

用途：
初始化永久保留池

---

check_keep_pool.py

用途：
檢查永久保留池

---

# Watchlist

create_watchlist_master.py

用途：
建立觀察群組

---

create_watchlist_stocks.py

用途：
建立群組成員表

---

add_watchlist.py

用途：
新增觀察群組

---

add_watchlist_stock.py

用途：
新增股票到群組

---

view_watchlist.py

用途：
查看觀察群組

---

# Daily Analysis

view_indicators.py

用途：
下載股價
計算：

- MA20
- MA60
- RSI
- MACD

並寫入資料庫

---

ai_analyze.py

用途：
AI 評分分析

---

modules/ai_score_engine.py

用途：
AI Score Engine

---

modules/ranking_engine.py

用途：
股票排名

---

build_selected_pool.py

用途：
建立每日推薦池

---

show_final_pool.py

用途：
顯示最終投資池

---

# Report

daily_report.py

用途：
產生報表

---

export_daily_report.py

用途：
輸出 TXT 報表

---

send_email_report.py

用途：
Email 推播

---

telegram_ai.py

用途：
Telegram Bot

---

test_telegram.py

用途：
測試 Telegram

---

# Backtest

backtest.py

用途：
歷史回測

---

# Monitoring

monitor.py

用途：
監控系統狀態

---

# Future Reserved

V4

- Top10 Sector Ranking
- Macro Risk Score

V5

- PostgreSQL
- NAS Data Lake
- n8n

V6

- AnythingLLM
- AI Research Report

V7

- YouTube Analysis
- News Sentiment
- AI Strategy Generator
