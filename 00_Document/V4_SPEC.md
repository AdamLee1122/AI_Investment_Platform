把目前已確認的內容全部寫進去：

- 台股1980+

- 美股3000+

- Top10類股選股

- 永久保留池

- NFP風險指標

- 失業率風險指標

- Fed升降息風險指標

- Telegram通知

- 每日自動更新

- AI綜合評分

- NAS同步

這份未來會成為 V4 的唯一正式規格文件。

接下來等你貼出 `telegram_ai.py` 全部程式碼後，就可以開始規劃真正的 V4 專案目錄與模組拆分，不會做到一半又推倒重來。



這是 V4 架構的重要里程碑。

目前流程已變成：

stock_master
      ↓
view_indicators.py
      ↓
Yahoo Finance
      ↓
技術指標
      ↓
AI Score
      ↓
SQLite
      ↓
Ranking

目前資料庫已經成功建立：

watchlist_master
    ↓
我的最愛
自選股1~4

watchlist_stocks
    ↓
各群組股票成員



目前狀態：



我的最愛
 ├─ 2330.TW
 └─ 2454.TW

自選股1
 └─ 2317.TW

自選股2
 └─ 2308.TW


