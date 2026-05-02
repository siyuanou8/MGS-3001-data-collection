
# MGS 3001 Data Collection Project

## Project Overview
This repository contains the data preparation files for my final project, "When AI Speaks, Markets Listen." The project studies how major large language model releases affected AI-related stock returns in the U.S. and Chinese markets.

## Research Question
Do major LLM releases generate different stock market reactions across U.S. and Chinese AI-related semiconductor and software firms?

## Data Sources
- U.S. stock data: collected through Python-based financial data tools
- Chinese A-share stock data: downloaded from the CSMAR database as CSV files
- U.S. market benchmark: S&P 500
- Chinese market benchmark: CSI 300
- News data: Chinese and English AI-related news datasets

## Final Dataset
The main dataset is `master_data.csv`.

Each row represents one firm-date observation. The dataset includes 60 AI-related listed firms across two markets, the U.S. and China, and two industries, semiconductor and software.

## Files
- `data_collection_v3.ipynb`: data collection and cleaning notebook
- `master_data.csv`: final merged dataset
- `cn_stock_data.csv`: cleaned Chinese stock data
- `us_stock_data.csv`: cleaned U.S. stock data
- `csi300_benchmark.csv`: Chinese market benchmark data
- `sp500_benchmark.csv`: U.S. market benchmark data
- `cn_news_raw.csv`: Chinese AI-related news data
- `en_news_raw.csv`: English AI-related news data

## Reproducibility
Run `data_collection_v3.ipynb` to reproduce the cleaned datasets and final `master_data.csv`.

## Reproducibility
Run `data_collection_v3.ipynb` to reproduce the cleaned datasets and final `master_data.csv`.
