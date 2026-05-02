# Data Description

The final dataset is `master_data.csv`. Each row represents one firm-date observation.

## Variable Dictionary

| Variable | Description |
|---|---|
| `date` | Trading date |
| `ticker` | Stock ticker |
| `market` | Market indicator, either `US` or `China` |
| `industry` | Industry group, either `Semi` or `Software` |
| `close` | Daily closing price |
| `log_ret` | Daily log return for U.S. stocks |
| `ret` | Daily return for Chinese stocks |
| `stock_ret` | Unified daily stock return variable used for later analysis |
| `volume` | Daily trading volume |
| `turnover` | Daily turnover rate |
| `marketcap` | Firm market capitalization |
| `beta` | Firm-level beta |
| `ret_market` | Daily market benchmark return |
| `China` | Dummy variable equal to 1 for Chinese firms |
| `Software` | Dummy variable equal to 1 for software firms |

## Notes

Chinese A-share stock data were downloaded from the CSMAR database because online APIs such as AKShare/TongHuaShun were unstable due to anti-scraping restrictions. The final dataset uses `stock_ret` as the unified stock return variable for later empirical analysis.
