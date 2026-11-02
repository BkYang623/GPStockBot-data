# GPStockBot-data

[GPStockBot](https://github.com/BkYang623/GPStockBot) 使用的公開資料，由 GPStockBot 的 GitHub Actions 排程自動更新，請勿手動修改。不同種類的資料放在不同資料夾。

## etf/：市值前 20 大 ETF 的每日持股

- 每個交易日（週一到週五）台灣時間 17:00 更新，只保留最近 92 天（約 3 個月）。
- `etf/holdings/ETF代號/資料日期.json`：當天的全部持股，每筆為 `{"name", "code", "weight", "shares"}`（名稱、代號、比例 %、持有股數；債券等沒有股數時為 null）。
- `etf/index.json`：每檔 ETF 有哪些日期，GPStockBot 依這份清單下載缺少的日子。
- 資料來源：MoneyDJ「全部持股」。僅供參考，不構成投資建議。
