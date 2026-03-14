# 🪙 Crypto ML Pipeline — Price Direction Prediction

An end-to-end machine learning pipeline for predicting cryptocurrency price direction using technical indicators and multiple ML models.

## 📊 Project Overview

This project investigates whether machine learning models can predict the daily price direction (up or down) of major cryptocurrencies using technical analysis indicators. The project also tests the **bear market hypothesis for 2026** — are we currently in a crypto bear market?

## 🪙 Cryptocurrencies Analyzed
- Bitcoin (BTC)
- Ethereum (ETH)
- BNB
- Solana (SOL)
- XRP

## 🛠️ Tech Stack
- **Python** — pandas, numpy, matplotlib
- **Machine Learning** — scikit-learn, LightGBM, pygam
- **Deep Learning** — PyTorch (LSTM)
- **Data** — yfinance, ta (technical analysis)

## 🤖 Models
| Model | Accuracy |
|---|---|
| LightGBM | 50.98% |
| LSTM (PyTorch) | 50.47% |
| SVM | 50.27% |
| GAM | 50.27% |
| Random Forest | 50.27% |

**LightGBM performs best** — gradient boosting is well suited for tabular financial data.

## 📐 Features (19 Technical Indicators)
- **Trend:** MA 50, MA 200, Golden/Death Cross
- **Momentum:** RSI, MACD, MACD Signal, MACD Diff
- **Volatility:** Bollinger Bands (High, Low, Width)
- **Price:** Daily Return, Log Return, High-Low Range, Price Change

## 🔍 Key Findings
1. **Volatility (BB_width) is the most important feature** — when the market is volatile, direction is easier to predict
2. **All models are bearish on BTC in 2026** — supporting the bear market hypothesis
3. **GAM is most bearish** — 99.71% probability of price going down
4. **Crypto markets are hard to predict** — all models hover around 50% accuracy, which is realistic and expected

## 📁 Project Structure
```
crypto-ml-pipeline/
├── notebooks/
│   ├── 01_EDA.ipynb                  # Data collection & exploration
│   ├── 02_feature-engineering.ipynb  # Technical indicators
│   ├── 03_models.ipynb               # Model training & comparison
│   └── 04_analysis.ipynb             # Analysis & conclusions
├── data/
│   ├── btc_usd_features.csv
│   ├── eth_usd_features.csv
│   ├── bnb_usd_features.csv
│   ├── sol_usd_features.csv
│   └── xrp_usd_features.csv
└── README.md
```

## 🚀 Future Work
- **Market Regime Detection** using Hidden Markov Models (HMM)
- **30-day price direction** prediction instead of daily
- **Streamlit dashboard** for interactive predictions
- **Big data pipeline** with Dask/Spark for tick-level data
- **Recursive forecasting** for multi-day predictions

## ⚠️ Disclaimer
This project is for educational purposes only. It is not financial advice. Cryptocurrency markets are highly unpredictable and past performance does not guarantee future results.