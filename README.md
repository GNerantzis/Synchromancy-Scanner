
# Synchromancy Scanner

<img width="1920" height="1021" alt="image" src="https://github.com/user-attachments/assets/44abc57a-a0c4-4a93-9202-0e7bb5bb5db4" />

A mechanical trend-following scanner for **Crypto, Stocks and Real Assets**, built around the **Synchromancy framework**.

The scanner automatically identifies bullish and bearish trends, optimizes parameters using historical performance and stability analysis, and presents a clean watchlist of the strongest candidates.

---

## Features

* Scan **Crypto**, **Stocks**, and **Real Assets**
* Separate **Weekly** and **Daily** tabs
* Synchromancy trend detection using **TradingView-style Supertrend**
* Automatic optimization:

  * Weekly: Best Supertrend Factor
  * Daily: Best ATR Length
* **ROI + Stability selection** to avoid overfitted parameters
* SQLite **Factor Cache** for dramatically faster rescans
* CoinGecko market-cap ranked crypto universe
* TradingView Screener integration for stocks
* Yahoo Finance integration for stocks and real assets
* TradingView chart links for every asset
* Bullish/Bearish highlighting
* Days and percentage since trend flip
* Excel export functionality
* **Dev View** toggle for advanced statistics

---

## Default View

Designed for everyday use, showing only the information required for decision-making:

* Asset
* Symbol
* Price
* Trend
* Flip Date
* Days Since Flip
* % Since Flip
* ROI %
* Market Cap / Category
* TradingView Link

---

## Dev View

Enable **Dev View** to expose optimization diagnostics:

* Winner ATR
* Winner Factor
* ROI Winner
* Stability Winner
* ROI Backtest %
* Stability Backtest %
* Stability Overrides
* Trade Counts
* Validity Flags
* Cache Age

---

## Stability Framework

The scanner uses a stability-weighted approach to reduce parameter overfitting.

Instead of selecting the parameter with the highest raw return, Synchromancy evaluates whether neighbouring parameters produce similar outcomes.

This favors **robust trends over fragile optimizations**.

---

## Requirements

* Python 3.11+
* PySide6
* pandas
* numpy
* yfinance
* ccxt
* requests
* tradingview-screener

Install dependencies:

```bash
pip install pandas numpy yfinance ccxt requests PySide6 tradingview-screener
```

---

## Building the Executable

```bash
python -m PyInstaller --onefile --windowed --icon=icon.ico synchromancy_scanner.py
```

---

## Disclaimer

Synchromancy Scanner is an educational and research tool.

It does **not** provide financial advice or guarantee future results. Always perform your own due diligence and use appropriate risk management.
