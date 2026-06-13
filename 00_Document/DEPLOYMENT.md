# DEPLOYMENT

最後更新：
2026-06-13

版本：
V4

---

# 開發環境

OS

Windows 11

---

Python

3.14

---

Database

SQLite

database/stock.db

---

Git

Git for Windows

---

GitHub Repository

AI_Investment_Platform

---

# 執行流程

每日執行：

run_daily.py

流程：

reset_db.py

↓

view_indicators.py

↓

build_selected_pool.py

↓

export_daily_report.py

↓

Telegram

↓

Email

---

# Telegram

用途：

每日通知

指令：

/daily

---

# Email

用途：

每日報表寄送

SMTP：

Gmail App Password

---

# 報表位置

reports/

例如：

daily_report_2026-06-13.txt

---

# Git 工作流程

每完成一個功能：

git add .

git commit -m "功能名稱"

git push origin main

---

查看狀態

git status

---

查看最近紀錄

git log --oneline -10

---

同步遠端

git pull origin main --rebase

---

# 備份策略

GitHub

每日同步

---

本地備份

04_Backup

---

未來

NAS 自動同步

---

# V5 Deployment

PostgreSQL

n8n

NAS

---

# V6 Deployment

AnythingLLM

Open WebUI

Ollama

---

# V7 Deployment

YouTube Analysis

Vector Database

AI Research Terminal
