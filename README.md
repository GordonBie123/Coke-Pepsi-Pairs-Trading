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

