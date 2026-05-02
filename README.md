# When AI Speaks, Markets Listen  
## Data Collection Repository

**Author:** Ou Siyuan  
**Course:** MGS 3001 WHS01  

## Research Question

Do major large language model releases generate different stock market reactions across U.S. and Chinese AI-related semiconductor and software firms?

## Project Overview

This repository contains the data collection and data preparation files for my final research project. The project studies how major LLM releases, especially GPT-4 and DeepSeek-R1, affected AI-related stock returns in the U.S. and Chinese markets.

## Dataset Description

The final dataset is `data/master_data.csv`.

Each row represents one firm-date observation. The dataset includes daily stock data for 60 AI-related listed firms across two markets: the U.S. and China. The firms are classified into two industries: semiconductor and software.

The dataset includes daily closing prices, stock returns, trading volume, turnover, market benchmark returns, market indicators, and industry classifications.

## Data Sources

- Chinese A-share stock data: CSMAR database, downloaded as CSV files
- U.S. stock data: collected through Python-based financial data tools
- Chinese market benchmark: CSI 300
- U.S. market benchmark: S&P 500
- News data: collected from Chinese and English financial news sources using web requests and hidden API responses
- `data/event_level_data.csv`: firm-event level dataset containing CAR, PostCAR, TurnoverChange, and estimated beta.
- `data/daily_event_data.csv`: daily event-window dataset containing abnormal returns and event-day indexes.

## Repository Structure

```text
MGS-3001-data-collection/
├── README.md
├── data/
│   ├── master_data.csv
│   ├── cn_stock_data.csv
│   ├── us_stock_data.csv
│   ├── csi300_benchmark.csv
│   ├── sp500_benchmark.csv
│   ├── cn_news_raw.csv
│   └── en_news_raw.csv
├── code/
│   └── data_collection_v3.ipynb
└── docs/
    └── data_description.md
