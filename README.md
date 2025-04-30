# Backtesting Automated-chart pattern 
backtesting Automated chart pattern recognition using python 

# Trading Strategy Backtesting
# Overview
This project contains Python scripts for backtesting trading strategies on historical financial data using candlestick patterns. The strategies implemented include:

Bullish Engulfing Pattern: Detects bullish engulfing patterns to initiate buy trades.
Bullish Flag Pattern: Identifies bullish flag patterns with breakout confirmation for trading.
Double Bottom Pattern: Detects double bottom patterns to signal buy opportunities.

Each script performs backtesting with a 5% profit target and a 3% stop-loss, tracks the capital curve, and visualizes trades using Plotly.
Prerequisites

Python 3.11 or higher
Google Colab (or a local Python environment with Jupyter Notebook support)
Historical OHLC (Open, High, Low, Close) data in Excel or CSV format

Installation

Clone or Download the Repository:If hosted on GitHub, clone the repository:
# git clone https://github.com/your-repo/trading-strategy-backtesting.git

Otherwise, download the scripts and data files manually.

Install Dependencies:Install the required Python packages using pip:
pip install pandas plotly numpy matplotlib mplfinance conda-package-handling

 Install TA-Lib (Optional, for advanced technical analysis):Follow the steps below to install TA-Lib in a Colab environment:
 url = 'https://anaconda.org/conda-forge/libta-lib/0.4.0/download/linux-64/libta-lib-0.4.0-h166bdaf_1.tar.bz2'
 !curl -L $url | tar xj -C /usr/lib/x86_64-linux-gnu/ lib --strip-components=1
 !pip install conda-package-handling
 !wget https://anaconda.org/conda-forge/ta-lib/0.5.1/download/linux-64/ta-lib-0.5.1-py311h9ecbd09_0.conda
 !cph x ta-lib-0.5.1-py311h9ecbd09_0.conda
 !mv ./ta-lib-0.5.1-py311h9ecbd09_0/lib/python3.11/site-packages/talib /usr/local/lib/python3.11/dist-packages/


# Set Up Historical Data:

Place your historical OHLC data files in the /content/drive/MyDrive/datasets/ directory (if using Colab).
Example files: 2024-01-1h.xlsx, 2024-02-1h.xlsx, BTCUSDT-1h-2024-12.csv.

# Open in Colab:

Upload the scripts to Google Colab.
Mount your Google Drive to access the dataset:from google.colab import drive
drive.mount('/content/drive')

# Run the Scripts:

Execute each script in a Colab cell.
Update the file_path variable in each script to point to your historical data file

# Files

bullish_engulfing_backtest.py: Backtests a strategy using the Bullish Engulfing pattern on January 2024 hourly data.
bullish_flag_backtest.py: Backtests a strategy using the Bullish Flag pattern on February 2024 hourly data, with visualizations of flagpoles and buy/sell signals.
double_bottom_backtest.py: Backtests a strategy using the Double Bottom pattern on December 2024 hourly data.
flagpole_visualization.py: Generates a simple Matplotlib plot to visualize a flagpole with a 45-degree angle.

# Dependencies

pandas: For data manipulation and analysis.
plotly: For interactive visualizations (candlestick charts and capital curves).
numpy: For numerical computations (e.g., angle calculations in the Bullish Flag pattern).
matplotlib: For plotting the flagpole visualization.
mplfinance: For additional financial plotting (installed but not used in the scripts).
ta-lib: For technical analysis (optional, installed but not used in the scripts).

# Sample Output
Bullish Engulfing Pattern (January 2024)
===== Trade Log =====
BUY at 42715.54 on 2024-01-01 13:00:00+00:00 - Profit/Loss: N/A
SELL at 45056.0 on 2024-01-02 00:00:00+00:00 - Profit/Loss: 547.9176899086373


# Notes

Ensure your historical data includes columns: Timestamp, Open, High, Low, Close.
The Bullish Flag script includes debug logs to help identify pattern detection and breakout conditions.
Adjust the flagpole_lengths, flag_lengths, profit_threshold, and stop_loss parameters to fine-tune the strategies.
Visualizations are displayed in a dark theme using Plotly's plotly_dark template.

License
This project is licensed under the MIT License.

