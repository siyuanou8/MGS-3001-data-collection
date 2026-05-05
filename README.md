# When AI Speaks, Markets Listen  
## Data Collection Repository

**Author:** Ou Siyuan  
**Course:** MGS 3001 WHS01  

## Research Question

Do major LLM releases generate different stock market reactions across U.S. and Chinese AI-related semiconductor and software firms?

## Project Overview

This repository contains the data collection and preparation files for my final research project. The project studies how GPT-4, Gemini, and DeepSeek-R1 affected AI-related stock returns in the U.S. and Chinese markets.

## Dataset Description

The main dataset is `data/master_data.csv`. It is a firm-date daily panel dataset covering 80 AI-related listed firms: 20 U.S. semiconductor firms, 20 U.S. software firms, 20 Chinese semiconductor firms, and 20 Chinese software firms.

The repository also includes:

- `data/event_level_data.csv`: firm-event level dataset containing CAR, PostCAR, TurnoverChange, TurnoverChangeRatio, and estimated beta.
- `data/daily_event_data.csv`: daily event-window dataset containing abnormal returns and event-day indexes.
- `data/sp500_benchmark.csv`: U.S. market benchmark data.
- `data/csi300_benchmark.csv`: Chinese market benchmark data.
- `data/cn_news_raw.csv` and `data/en_news_raw.csv`: AI-related news data used for event context and narrative interpretation.

## Data Sources

- U.S. stock data: collected through Python-based financial data tools.
- Chinese A-share stock data: downloaded from CSMAR as CSV files.
- U.S. benchmark: S&P 500.
- Chinese benchmark: CSI 300.
- News data: collected from Chinese and English financial news websites using browser DevTools, hidden API requests, and Python requests.

## Repository Structure

```text
MGS-3001-data-collection/
├── README.md
├── data/
│   ├── master_data.csv
│   ├── event_level_data.csv
│   ├── daily_event_data.csv
│   ├── sp500_benchmark.csv
│   ├── csi300_benchmark.csv
│   ├── cn_news_raw.csv
│   └── en_news_raw.csv
├── code/
│   └── data_collection_v3.ipynb
└── docs/
    └── data_description.md
