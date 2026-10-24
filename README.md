# Multi-Asset Volatility & Maximum Drawdown Analysis (Python)

## Project Overview
A quantitative market risk analysis script built in **Python (`pandas`, `numpy`, `yfinance`)** that evaluates historical price volatility and downside drawdown risk across five major global asset classes over a 1-year lookback period:
* **Crypto:** Bitcoin (`BTC-USD`)
* **Macro / Currency Index:** US Dollar Index (`DX-Y.NYB`)
* **Major Forex:** Euro / US Dollar (`EURUSD=X`)
* **US Equities:** Apple (`AAPL`) & Tesla (`TSLA`)

## Key Analytical Workflow
1. **Automated Data Pipeline & Calendar Alignment:** Pulls daily closing prices via the Yahoo Finance API (`yfinance`) and applies forward-filling (`ffill`) to align 24/7 cryptocurrency trading days with the 5-day traditional equity and FX calendar.
2. **Daily & Annualized Volatility:** Computes daily percentage returns and calculates both average daily return standard deviation and annualized volatility (`Daily Volatility × √252`).
3. **Peak-to-Trough Maximum Drawdown (MDD):** Tracks the running high-water mark (`cummax`) for each asset to measure its worst historical percentage drop from a peak—helping risk managers compare tail risk between high-beta assets (BTC, TSLA) and low-volatility currency pairs (EUR/USD, DXY).

## Tools & Libraries Used
* Python 3 (Google Colab / Jupyter Notebook)
* `yfinance` for live historical market data retrieval
* `pandas` & `numpy` for time-series cleaning and risk calculations
