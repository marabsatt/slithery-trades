# Stock Market Portfolio Optimization using Riskfolio and Interactive Brokers

## Overview

This project demonstrates a fully automated pipeline for constructing and optimizing a portfolio using NASDAQ-100 and S&P 500 stocks. It leverages real-time market data through the Interactive Brokers API and applies modern portfolio theory via the `Riskfolio-Lib` library.

## Objectives

- Retrieve and process live market data for NASDAQ-100 and S&P 500 companies.
- Construct a financial portfolio with diversification and risk-return optimization.
- Use `Riskfolio-Lib` to apply advanced optimization techniques such as:
  - Mean-Variance Optimization (MVO)
  - Risk Parity
  - Conditional Value at Risk (CVaR)
- Integrate with Interactive Brokers for live market access.

## Frameworks Used
See requirements.txt for full list

- **Python**
- **Pandas / NumPy** for data manipulation
- **yFinance** for historical financial data
- **IB_insync** for real-time trading via Interactive Brokers
- **Riskfolio-Lib** for portfolio optimization
- **Matplotlib** for data visualization
- **BeautifulSoup / pandas.read_html** for web scraping

## Data Sources

- NASDAQ-100 constituents scraped from [Wikipedia](https://en.wikipedia.org/wiki/NASDAQ-100)
- S&P 500 constituents scraped from [Wikipedia](https://en.wikipedia.org/wiki/List_of_S%26P_500_companies)
- Historical price data via `yfinance`
- Real-time market data via Interactive Brokers API (TWS / IB Gateway)

## Key Steps

1. **Initialization**:
   - Connect to Interactive Brokers using `ib_insync`
   - Apply `nest_asyncio` to enable nested event loops in Jupyter

2. **Data Retrieval**:
   - Scrape NASDAQ-100 tickers from Wikipedia
   - Scrape S&P 500 tickers from Wikipedia
   - Retrieve historical prices using `yfinance`
   - Real-time data access through Interactive Brokers

3. **Portfolio Construction**:
   - Filter, clean, and structure the price data
   - Calculate returns and covariance matrices
   - Use `Riskfolio-Lib` to optimize the portfolio

4. **Visualization**:
   - Efficient frontier plots
   - Risk contribution charts
   - Asset allocation visualizations

## Setup

**IBKR Confifuration**:
- TWS or IB Gateway running locally (default port 7497)
- A valid Interactive Brokers account (paper trading works)

**Running the Notebook**:
- Open 'main.ipynb' in Jupyter and run the cells sequentially. Ensure your IB Gateway is connected before starting.

## Disclaimer
- *This project is intended for educational and research purposes.*
- *Real trading should be approached cautiously; backtesting and paper trading are recommended before deployment to a production environment.*
- *Some elements may require further enhancement for production use, such as exception handling, logging, and parameter tuning.*

### Prerequisites

Install required libraries via pip:

```bash
pip install yfinance ib_insync riskfolio-lib nest_asyncio waiting


