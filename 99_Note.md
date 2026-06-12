AI 不要偏離軌道


### 如果目標是真正的 24 小時 AI 投資研究平台

我會把未來版本規劃成：

**V4**

- 台股+美股

- 類股 Top10

- 永久保留池

- 總經風險指標

- Telegram 推播

**V5**

- NAS 資料湖

- AnythingLLM 整合

- 自動研究報告

- PDF/PPT 郵件寄送

**V6**

- YouTube 分析

- 新聞情緒分析

- 關聯性評分模型

- AI 研究助理

**V7**

- AI 自動生成投資策略

- AI 自動回測

- AI 自動優化選股條件

- AI 長期記憶系統

到 V7 時，就比較像個人版的 AI Research Terminal，而不只是選股程式了。

顯示較少

我還需要搭配什麼軟體嗎 比方說 n8n, codex 等等 之類的

ChatGPT上午4:26

如果你的目標是做到「24小時 AI 投資研究平台」，我會建議分層建設，不要一次裝太多工具。

### 核心層（必裝）

#### 1. AnythingLLM

用途：

- 建立長期知識庫

- 查詢歷史報告

- 問答分析

你已經有了 ✅

---

#### 2. n8n

用途：

- 自動化工作流

- 定時執行

- 串接 Email、Telegram、NAS、AI

例如：

```
每天 06:00    ↓抓台股美股資料    ↓AI分析    ↓產生報告    ↓寄Email    ↓Telegram摘要
```

我認為這是下一個最值得安裝的。

---

#### 3. PostgreSQL

用途：

取代大量 JSON

目前：

```
market.jsonperformance.json
```

未來幾百萬筆資料後：

```
PostgreSQL
```

查詢速度會快很多。

---

### 第二層（V5~V6）

#### 4. Ollama

本地 AI

例如：

- DeepSeek

- Qwen

- Llama

優點：

- 不用一直付 API 費

- 24小時運作

AnythingLLM 可以直接串。

---

#### 5. Open WebUI

類似 ChatGPT 的本地介面

搭配：

```
Ollama+AnythingLLM
```

很好用。

---

### 第三層（資料湖）

#### 6. NAS

你的 NAS 未來很重要。

建議用途：

```
/NAS    /stock    /macro    /youtube    /news    /reports    /backtest
```

變成 AI Data Lake。

---

### 第四層（進階）

#### 7. YouTube 分析

工具：

```
yt-dlpyoutube-transcript-apiWhisper
```

流程：

```
抓影片↓字幕↓AI摘要↓寫入AnythingLLM
```

這是未來最有價值的另類資料來源之一。

---

### 8. 向量資料庫

當資料量爆增後：

- ChromaDB

- Qdrant

- Weaviate

讓 AI 可以搜尋：

> 「過去三年提到 CoWoS 的所有新聞、影片、報告」

---

### 關於 Codex

如果你說的是 OpenAI 的 Codex 類工具：

用途偏向

```
寫程式修改程式除錯
```

對你的平台有幫助，但優先度沒有：

```
n8nPostgreSQLNASAnythingLLM
```

高。

---

如果是我幫你排優先順序：

```
現在↓完成 V4 股票系統接著↓n8n接著↓NAS接著↓PostgreSQL接著↓AnythingLLM整合接著↓YouTube分析接著↓向量資料庫最後↓本地LLM(Ollama)
```

這樣會比較穩，不會一次把系統複雜度拉太高。

顯示較少

@ChatGPT 會不會完成 V4 之後, 你就會忘記 V5~V7 要做些什麼, 我有什麼方法不要讓這個斷層產生嗎?

ChatGPT上午4:28

會有這個風險。

因為我不會自動保留你專案的長期狀態，也不會在未來自動記得 V4 討論出的所有細節。如果隔幾週或幾個月後重新開新對話，我看到的內容可能不完整。

比較好的做法是把專案本身變成「可被 AI 接手的文件」。

建議建立一個：

```
AI_Investment_Platform/│├─ PROJECT_MASTER.md├─ ROADMAP.md├─ ARCHITECTURE.md├─ TODO_V4.md├─ TODO_V5.md├─ TODO_V6.md├─ TODO_V7.md└─ CHANGELOG.md
```

例如：

### PROJECT_MASTER.md

記錄：

- 專案目標

- 系統架構

- 資料來源

- NAS規劃

- AnythingLLM規劃

- Telegram規劃

- Email/PPT規劃

---

### ROADMAP.md

```
V4✓ 台股1980+✓ 美股3000+✓ Top10分類選股✓ 永久保留池✓ 風險指標V5□ PostgreSQL□ NAS資料湖□ n8n自動化V6□ AnythingLLM整合□ AI研究報告□ PPT自動生成V7□ YouTube分析□ 向量資料庫□ 多模型AI評分
```

---

### CHANGELOG.md

每次修改都記錄：

```
2026-06-09新增：- 美股掃描- 非農風險指標- 永久保留池修改：- Top100改成類股Top10
```

---

如果未來接入 AnythingLLM，效果更好：

```
PROJECT文件+歷史報告+程式碼+資料庫
```

全部丟進知識庫。

之後你問：

> V6做到哪了？

AI 可以直接從知識庫查。

---

以你目前的規模，我認為最重要的不是先做 V5，而是先建立一份「PROJECT_MASTER.md」。

只要這份文件維護得好，即使換 AI、換電腦、換模型，專案都不會斷層。

顯示較少

請引導我建立 "可被 AI 接手的文件"
越詳細越好, 之後再陸續完成V4, V5~V7

ChatGPT上午4:31

這是我建議你直接建立的第一版架構。

## 第一步：建立專案總目錄

```
D:\AI_Investment_Platform\│├─ 00_Document├─ 01_SourceCode├─ 02_Data├─ 03_Report├─ 04_Backup├─ 05_AnythingLLM├─ 06_NAS_SYNC└─ 07_Config
```

---

# 00_Document

這是最重要的資料夾。

```
00_Document│├─ PROJECT_MASTER.md├─ ARCHITECTURE.md├─ ROADMAP.md├─ CHANGELOG.md├─ STOCK_CATEGORY.md├─ AI_SCORING.md├─ DATA_SOURCE.md└─ DEPLOYMENT.md
```

---

# PROJECT_MASTER.md

這份是整個系統的大腦。

```
# AI Investment Platform建立日期：2026-06-09建立者：Adam Lee---# 專案目標打造24小時AI投資研究平台涵蓋：- 台股- 美股- ETF- 總經- AI分析- Telegram通知- Email報告- NAS資料湖- AnythingLLM知識庫---# 系統版本目前版本：V4下一版本：V5V6V7
```

---

# ROADMAP.md

記錄未來版本。

```
# V4## 已完成[ ]## 開發中[ ] 台股1980+[ ] 美股3000+[ ] Top10分類選股[ ] 永久保留池[ ] Telegram通知---# V5[ ] PostgreSQL[ ] NAS資料湖[ ] n8n自動化---# V6[ ] AnythingLLM[ ] AI研究報告[ ] PowerPoint自動生成---# V7[ ] YouTube分析[ ] 新聞情緒分析[ ] 多模型AI評分
```

---

# ARCHITECTURE.md

未來所有AI都看這份。

```
資料來源Yahoo FinanceFedFREDFinvizSECYouTube↓每日收集↓本地電腦↓NAS↓資料庫↓AnythingLLM↓AI分析↓Telegram↓Email↓PPT
```

---

# STOCK_CATEGORY.md

這份很重要。

未來 Top100 改成類股 Top10 就靠它。

```
# 半導體2330 台積電2454 聯發科NVDAAMDTSM---# AINVDAMSFTGOOGLMETA---# 設備ASMLAMATLRCX---# 光學大立光玉晶光---# 面板群創友達彩晶
```

之後 AI 可以直接依類股分析。

---

# AI_SCORING.md

定義評分規則。

例如：

```
# AI評分技術面40%基本面25%籌碼面15%總經面10%市場情緒10%
```

---

# DATA_SOURCE.md

記錄所有資料來源。

```
股價Yahoo Finance非農FRED失業率FRED利率FEDCPIFRED新聞News APIYouTubeYouTube API
```

---

# CHANGELOG.md

每次修改都寫。

```
2026-06-09新增- 美股3000掃描- 永久保留池- NAS規劃修改- Top100改成類股Top10
```

---

# 第二步：建立資料湖(Data Lake)

```
02_Data│├─ TW├─ US├─ Macro├─ News├─ YouTube├─ Backtest└─ AI_Result
```

例如：

```
02_Data └─ Macro      ├─ CPI      ├─ NFP      ├─ Unemployment      ├─ FedRate      └─ GDP
```

這樣未來累積 5~10 年資料都不會亂。

---

# 第三步：建立 NAS 架構

```
NAS│├─ RawData├─ Database├─ Report├─ PPT├─ AI_Knowledge└─ Backup
```

同步方式：

```
本地電腦↓每日分析↓NAS同步↓AnythingLLM讀取
```

---

# 第四步：建立 AI 知識庫

未來 AnythingLLM 匯入：

```
PROJECT_MASTER.mdROADMAP.mdARCHITECTURE.md歷史報告歷史回測市場資料YouTube逐字稿新聞摘要
```

之後你直接問：

> 過去三年 AI 類股勝率最高的是什麼？

AI 就能查自己的資料庫回答。








