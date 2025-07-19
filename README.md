# 📈 RSI Divergence + BoS/ChoCH + Order Block (SMC) Strategy

This repository implements a Smart Money Concepts (SMC)-inspired quantitative trading strategy for **EUR/USD**, combining:

- **RSI Divergence** (for early signal detection)
- **Break of Structure (BoS)** and **Change of Character (ChoCH)** (for trend confirmation)
- **Order Block Retracement Entries** (for refined entries and better risk-reward)

All analysis is done using Python, Pandas, and Matplotlib, with price data from Yahoo Finance.

---

## 📘 Notebooks Overview

| Notebook | Description |
|----------|-------------|
| `01_rsi_divergence_smc_strategy.ipynb` | End-to-end example of the RSI + SMC strategy with initial logic |
| `02_detect_rsi_divergence.ipynb` | Detect bullish and bearish RSI divergence patterns |
| `03_detect_bos_choch.ipynb` | Identify BoS and ChoCH based on swing structure |
| `04_backtest_rsi_smc.ipynb` | Backtesting the full strategy based on RSI + BoS/ChoCH |
| `05_ob_retest_strategy.ipynb` | Enter trades only after retracement to valid Order Block following ChoCH |

---

## ⚙️ Strategy Rules

### ✅ Entry Conditions
- **W pattern** (bullish): Price makes a lower low while RSI makes a higher low
- **M pattern** (bearish): Price makes a higher high while RSI makes a lower high
- **BoS/ChoCH**: Confirms the reversal
- **Order Block Retest**: Price returns to last opposite candle before ChoCH

### 🎯 Exit Conditions
- **Take Profit**: Previous high/low after ChoCH
- **Stop Loss**: Opposite side of the Order Block

---

## 📊 Backtest Metrics
Each trade records:
- Entry Time
- Entry Price
- Take Profit (TP)
- Stop Loss (SL)
- Win/Loss Outcome
- Result Chart

---

## 📦 Requirements

Install all dependencies using:

```bash
pip install pandas numpy yfinance matplotlib

