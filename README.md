# A-Share MOM20 Factor Research

## Overview

This project investigates whether stocks with higher returns over the past 20 trading days tend to outperform over the following 5 trading days.

The study examines a selected sample of 50 Chinese A-share stocks using daily price data from 2023 to 2025.

## Methodology


### Factor Definition

$$
MOM20_{i,t} = \frac{P_{i,t}}{P_{i,t-20}} - 1
$$

### Forward Return

$$
R_{i,t\rightarrow t+5} = \frac{P_{i,t+5}}{P_{i,t}} - 1
$$


The analysis includes:

- Data cleaning and trading-date alignment
- Cross-sectional quintile sorting
- Average forward returns and Q5–Q1 spread
- Daily Spearman RankIC and ICIR
- Year-by-year stability analysis
- Research visualizations

## Key Findings

| Metric | Result |
|---|---:|
| Mean RankIC | -0.02553 |
| RankIC ICIR (unannualized) | -0.1047 |
| RankIC Positive Ratio | 48.58% |
| Average Q5–Q1 Spread | -0.0768 percentage points |

The sample does not demonstrate a stable positive relationship between 20-day momentum and subsequent 5-day returns. Results vary across years.

These findings are descriptive and do not establish statistical significance or trading profitability.

## Tools

Python, pandas, NumPy, Matplotlib, Jupyter Notebook

## Data Source

Daily A-share stock data obtained using the `free-stockdb` project and its Python SDK.

The raw market database is not included in this repository. Reproduction requires access to the corresponding data source and SDK, as well as adjustment of local file paths.

## Limitations

- Limited sample size and non-representative stock selection
- Price-adjustment methodology not independently verified
- Overlapping five-day forward-return windows
- No formal statistical significance or out-of-sample tests
- No transaction-cost or executable portfolio backtest

## Notebook

See **MOM20_Factor_Research.ipynb** for the full analysis.
