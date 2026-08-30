# constrained-portfolio-optimisation
Python-based constrained portfolio optimisation using historical market data and Sharpe-ratio maximisation.

# Constrained Portfolio Optimisation

## Overview

This project develops a Python-based constrained portfolio optimisation model that aims to identify portfolio weights that maximise the Sharpe ratio while satisfying predefined allocation constraints.

The analysis also examines whether the optimised portfolio provides stronger historical risk-adjusted performance than a simple equally weighted portfolio.

> **Disclaimer:** This project is for educational purposes only and does not constitute investment advice.

## Objectives

- Collect historical market data using Python
- Calculate daily logarithmic returns
- Estimate annualised covariance
- Calculate portfolio volatility
- Estimate a risk-free rate using FRED
- Optimise portfolio weights using the Sharpe ratio
- Apply portfolio allocation constraints
- Compare the optimised portfolio with an equal-weight benchmark
- Analyse asset correlations and diversification

## Investment Universe

| Ticker | Exposure | Portfolio Role |
|---|---|---|
| SPY | S&P 500 | Large-cap US equities |
| BND | US bonds | Fixed-income diversification |
| GLD | Gold | Alternative/defensive exposure |
| QQQ | Nasdaq-100 | Growth and technology exposure |
| VTI | Total US stock market | Broad US equity exposure |

## Methodology

Historical adjusted closing prices are collected using `yfinance`.

Daily logarithmic returns are calculated and used to estimate the annualised covariance matrix.

The Sharpe ratio is then maximised using SciPy's SLSQP optimisation algorithm, subject to:

- Portfolio weights summing to 100%
- No short selling
- Maximum 40% allocation to any individual asset

The resulting portfolio is compared with a 20%-per-asset equal-weight benchmark.

## Technologies

- Python
- Pandas
- NumPy
- SciPy
- Matplotlib
- yfinance
- FRED API
- Google Colab

## Key Analysis

The project evaluates:

- Expected annual return
- Annualised volatility
- Sharpe ratio
- Optimised portfolio weights
- Equal-weight benchmark performance
- Asset return correlations

## Limitations

The model relies on historical estimates, which may not represent future market conditions.

The optimal allocation is sensitive to the chosen historical period, expected-return estimates, covariance structure and risk-free-rate assumption.

The model also does not account for transaction costs, taxes, market impact or tail-risk measures.

## Future Development

Future versions of this project can incorporate more advanced risk-management techniques, including:

- Value at Risk (VaR)
- Expected Shortfall
- Historical stress testing
- Asset-specific stress scenarios
- Drawdown analysis
- Out-of-sample testing
- Reverse stress testing
