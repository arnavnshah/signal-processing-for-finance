# FFT-Based Statistical Arbitrage using Signal Processing

> Applying Digital Signal Processing (DSP) techniques to Quantitative Finance using Fast Fourier Transform (FFT) for volatility-aware pairs trading.

---

## Overview

This project explores the intersection of **Signal Processing** and **Quantitative Finance** by integrating Fast Fourier Transform (FFT) into a classical statistical arbitrage framework.

A traditional pairs trading strategy is enhanced using frequency-domain analysis to identify noisy market regimes and suppress low-quality trading signals. The project evaluates whether spectral filtering can improve the risk-adjusted performance of a mean-reversion strategy.

---

## Problem Statement

Classical pairs trading strategies often generate false trading signals during periods of elevated market volatility. These noisy signals increase drawdowns and reduce overall strategy robustness.

This project investigates whether **FFT-based spectral analysis** can distinguish between genuine trading opportunities and high-frequency market noise.

---

## Methodology

The project follows the pipeline below:

1. Acquire historical price data using Yahoo Finance
2. Select highly correlated equity pairs
3. Estimate hedge ratio using Ordinary Least Squares (OLS)
4. Perform Engle-Granger Cointegration Test
5. Construct the spread between paired assets
6. Generate Rolling Z-Score trading signals
7. Apply Fast Fourier Transform (FFT)
8. Compute rolling spectral energy ratio
9. Detect high-volatility market regimes
10. Filter trading signals using frequency-domain information
11. Backtest baseline and FFT-filtered strategies
12. Compare cumulative returns and drawdowns

---

## Features

- Statistical Arbitrage (Pairs Trading)
- Fast Fourier Transform (FFT)
- Cointegration Testing
- Rolling Z-Score Strategy
- Frequency-Domain Volatility Filtering
- Regime Detection
- Strategy Backtesting
- Out-of-Sample Validation
- Performance Comparison

---

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Statsmodels
- yfinance
- Jupyter Notebook

---

## Project Structure

```
signal-processing-for-finance/
│
├── notebooks/
│   └── analysis.ipynb
│
├── data/
│   └── market_data.csv
│
├── figures/
│   ├── zscore.png
│   ├── fft_spectrum.png
│   ├── equity_curve.png
│
├── report/
│   └── Project_Report.pdf
│
├── README.md
└── requirements.txt
```

---

## Results

The FFT-based filter successfully identified periods of elevated market noise and reduced equity curve volatility.

Key observations:

- Reduced drawdowns during highly volatile periods
- Smoother equity curve compared to baseline strategy
- Effective volatility regime detection using rolling FFT
- Lower overall returns due to suppression of profitable high-volatility trades
- Demonstrated the trade-off between risk reduction and return generation

---

## Key Concepts

- Statistical Arbitrage
- Pairs Trading
- Mean Reversion
- Cointegration
- Hedge Ratio Estimation
- Fast Fourier Transform (FFT)
- Frequency-Domain Signal Processing
- Rolling Window Analysis
- Volatility Filtering
- Quantitative Finance

---

## Future Improvements

- Kalman Filter-based dynamic hedge ratios
- Machine Learning-based regime classification
- Multi-asset portfolio implementation
- Transaction cost optimization
- High-frequency data analysis
- Real-time trading dashboard
- Performance optimization for live deployment

---

## Disclaimer

This project was developed for academic purposes as part of the Signals and Systems (ECE F243) course at BITS Pilani, Goa Campus.

It is intended for research and educational purposes only and should not be interpreted as financial or investment advice.

---

