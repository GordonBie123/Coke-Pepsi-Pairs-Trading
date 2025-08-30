# Coca-Cola and Pepsi Pairs Trading Strategy

A statistical arbitrage trading strategy that exploits the mean-reverting relationship between Coca-Cola (KO) and Pepsi (PEP) stock prices.

## Overview

This project implements a market-neutral pairs trading strategy using cointegration analysis and z-score based signals. The strategy identifies when the price relationship between KO and PEP deviates from historical norms and trades on the assumption that the relationship will revert to the mean.

## Key Features

- Cointegration testing using Engle-Granger methodology
- Dynamic hedge ratio calculation using OLS regression
- Rolling z-score signal generation
- Comprehensive backtesting framework with transaction costs
- Parameter optimization across multiple window sizes and thresholds
- Performance analytics including Sharpe ratio, maximum drawdown, and profit factor

## Results

- **Total Return**: 12.45% over 5 years
- **Annualized Return (CAGR)**: 2.37%
- **Sharpe Ratio**: 0.89
- **Maximum Drawdown**: 8.23%
- **Win Rate**: 52%
- **Profit Factor**: 1.25

## Usage

1. Clone the repository
2. Install required packages: `pip install -r requirements.txt`
3. Run the Jupyter notebook `pairs_trading_ko_pep.ipynb`

## Strategy Components

### 1. Data Collection
- Downloads 5 years of daily adjusted close prices for KO and PEP
- Data period: 2019-01-01 to 2024-01-01

### 2. Statistical Analysis
- Tests for stationarity using Augmented Dickey-Fuller test
- Verifies cointegration between the two time series
- Calculates optimal hedge ratio using ordinary least squares

### 3. Signal Generation
- Computes spread between KO and hedge-ratio-adjusted PEP
- Calculates rolling z-score with configurable window
- Generates entry signals when z-score exceeds thresholds
- Exits positions when z-score reverts to mean

### 4. Backtesting
- Simulates trading with realistic transaction costs (0.1%)
- Tracks positions and calculates daily returns
- Compares performance against buy-and-hold benchmark

### 5. Parameter Optimization
- Tests window sizes: 30, 60, 90, 120 days
- Tests entry thresholds: 0.5, 1.0, 1.5, 2.0 standard deviations
- Identifies optimal parameters based on Sharpe ratio

## Files

- `cokepeptrade.ipynb` - Main Jupyter notebook with full implementation
- `requirements.txt` - Python package dependencies
- `README.md` - This file

## Visualizations

The notebook generates several plots to analyze the strategy:
- Price series comparison
- Spread analysis with confidence bands
- Rolling z-score with trading signals
- Position chart showing long/short periods
- Cumulative returns vs benchmark
- Drawdown analysis
- Parameter optimization heatmap

## Limitations

- Past performance does not guarantee future results
- Strategy assumes the KO-PEP relationship remains stable
- Does not account for market regime changes
- Transaction costs are simplified estimates
- Does not include borrowing costs for short positions

## Future Improvements

- Implement dynamic hedge ratio updates
- Add stop-loss mechanisms
- Include regime detection to pause trading during relationship breakdowns
- Expand to multiple pairs for portfolio diversification
- Add real-time trading capabilities

## Author

Gordon Bie

## License

This project is for educational purposes only. Use at your own risk.
