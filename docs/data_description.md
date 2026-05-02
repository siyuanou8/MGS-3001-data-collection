# Data Description

The final dataset is `data/master_data.csv`. Each row represents one firm-date observation.

## Data Sources

- **Chinese A-share stock data:** CSMAR database, downloaded as CSV files.
- **U.S. stock data:** collected through Python-based financial data tools.
- **Chinese market benchmark:** CSI 300 benchmark data.
- **U.S. market benchmark:** S&P 500 benchmark data.
- **News data:** collected from Chinese and English financial news sources using web requests and hidden API responses.

## Collection Method

This project uses both database CSV downloads and web-based data collection.

Chinese A-share stock data were originally attempted through AKShare/TongHuaShun. A single-stock test could return valid data, but batch collection for 30 Chinese stocks was unstable because repeated requests likely triggered anti-scraping restrictions. Therefore, the final Chinese stock data were downloaded from the CSMAR database as CSV files.

News data were collected by using browser DevTools to inspect Network requests, identify hidden API endpoints, and parse JSON responses with Python `requests`.

## Time Period Covered

The stock dataset covers daily observations from **2022-06-01** to **2026-04-30**.

## Dataset Size

The final dataset `master_data.csv` contains:

- **51,239 rows**
- **15 columns**
- **60 listed firms**
- **2 markets:** U.S. and China
- **2 industries:** Semiconductor and Software

## Variable Dictionary

| Variable | Data Type | Description | Example |
|---|---|---|---|
| `date` | Date | Trading date | `2022-06-01` |
| `ticker` | String | Stock ticker | `NVDA` |
| `market` | String | Market indicator | `US` |
| `industry` | String | Industry group | `Semi` |
| `close` | Float | Daily closing price | `18.2867` |
| `log_ret` | Float | Daily log return mainly for U.S. stocks | `0.0671` |
| `volume` | Float | Daily trading volume | `544514000` |
| `turnover` | Float | Daily turnover rate | `0.0224` |
| `marketcap` | Float | Firm market capitalization | `4.823327e+12` |
| `beta` | Float | Firm-level beta | `2.335` |
| `ret_market` | Float | Daily market benchmark return | `0.0183` |
| `ret` | Float | Daily return mainly for Chinese stocks | `0.0407` |
| `China` | Integer | Dummy variable equal to 1 for Chinese firms | `0` |
| `Software` | Integer | Dummy variable equal to 1 for software firms | `0` |
| `stock_ret` | Float | Unified stock return variable used for later analysis | `0.0671` |

## Known Data Quality Issues

- Chinese and U.S. markets follow different trading calendars.
- Return values are missing on the first trading day for each stock because returns require the previous closing price.
- Some benchmark returns are missing on non-overlapping market holidays.
- Chinese A-share batch collection through AKShare/TongHuaShun was unstable due to anti-scraping restrictions, so CSMAR CSV data were used instead.
- News data collection required hidden API requests; some websites used signed request parameters.
- The DeepSeek-R1 event date is close to the Chinese Spring Festival market closure, which may affect later event-window analysis.
