# 📊 Automated Chart Pattern Backtesting

Backtest popular candlestick and chart pattern strategies using Python on historical OHLC data. This project uses interactive visualizations, configurable risk-reward logic, and modular scripts for each strategy.

---

## 🧠 Strategy Overview

This repository implements and backtests the following technical trading strategies:

- **📈 Bullish Engulfing**  
  Detects bullish engulfing candlestick patterns to trigger buy trades.

- **🚩 Bullish Flag**  
  Identifies bullish flag patterns and executes trades on breakout confirmation.

- **💹 Double Bottom**  
  Recognizes double bottom patterns as potential reversal signals for buying.

All strategies use:

- **Profit Target**: 5%  
- **Stop Loss**: 3%  
- **Capital Curve Tracking**  
- **Trade Visualization**: Plotly for interactive charting

---

## 🛠️ Prerequisites

- Python 3.11+
- Google Colab (recommended) or a local Jupyter environment
- Historical OHLC data in `.csv` or `.xlsx` format

---

## 📥 Installation

### 🔹 Clone the Repository

```bash
git clone https://github.com/your-username/automated-pattern-backtest.git
cd automated-pattern-backtest
