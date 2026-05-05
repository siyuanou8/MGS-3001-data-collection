# Data Description

## Project Title

**When AI Speaks, Markets Listen**

## Research Question

Do major LLM releases generate different stock market reactions across U.S. and Chinese AI-related semiconductor and software firms?

## Final Datasets

This repository contains the final cleaned datasets used for the data collection and research readiness stage.

| Dataset | Rows | Columns | Description |
|---|---:|---:|---|
| `master_data.csv` | 76,814 | 15 | Final firm-date daily panel dataset |
| `event_level_data.csv` | 239 | 20 | Firm-event level event-study dataset |
| `daily_event_data.csv` | 36,089 | 20 | Daily event-window abnormal return dataset |
| `sp500_benchmark.csv` | benchmark data | benchmark data | U.S. market benchmark data |
| `csi300_benchmark.csv` | benchmark data | benchmark data | Chinese market benchmark data |
| `cn_news_raw.csv` | news data | news data | Chinese AI-related news headlines |
| `en_news_raw.csv` | news data | news data | English AI-related news headlines |

The main dataset is `master_data.csv`. It contains daily stock observations for 80 AI-related listed firms across two markets and two industries:

- U.S. semiconductor firms: 20
- U.S. software firms: 20
- Chinese semiconductor firms: 20
- Chinese software firms: 20

## Sample Expansion

The sample was expanded from 60 firms to 80 firms to improve statistical power for later empirical analysis. Each market-industry group now contains 20 firms.

The additional firms were selected based on three criteria:

1. **AI relevance**: firms must have clear exposure to AI-related semiconductor, software, cloud, enterprise software, cybersecurity, or AI application activities.
2. **Market capitalization or industry representativeness**: larger or more representative firms were prioritized within each market-industry group.
3. **Data availability**: firms needed sufficient daily trading data to construct the estimation window, event window, and post-event window.

## Event Coverage

The updated event-study design includes three major LLM release events:

| Event | Event Date | Origin |
|---|---:|---|
| GPT-4 | 2023-03-15 | U.S. |
| Gemini | 2023-12-06 | U.S. |
| DeepSeek-R1 | 2025-01-27 | China |

The planned event-level sample is:

```text
80 firms × 3 events = 240 firm-event observations
