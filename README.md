Stock Market Next Day Return Predictor — Machine Learning (NIFTY)

This project builds a machine learning model to **predict next-day NIFTY 50 returns** using historical market data and advanced technical indicator–based feature engineering.  
The goal is to explore how engineered financial signals and time-series patterns can improve short-term market forecasting.

Project Overview

This repository contains an end-to-end ML workflow for financial prediction, including:
- Data collection using **yfinance**
- Extensive **feature engineering**
- Model training (Random Forest Regressor, Linear Regression)
- Performance comparison and error analysis
- Visualizations of trends, predictions, and feature distributions

Data Source
- Historical NIFTY 50 index data fetched using the yfinance Python API.


Feature Engineering

The project uses multiple market technical indicators to extract useful patterns:

Trend & Momentum Indicators
- **Moving Averages (MA)**
- **Exponential Moving Averages (EMA 5/20/50)**
- **Relative Strength Index (RSI)**  
- **MACD Line + Signal Line**
- **Rate of Change (ROC)**

Volatility Indicators
- **Bollinger Bands (BBHIGH, BBLOW)**
- **Average True Range (ATR)**
- **Standard deviation windows**

Volume Indicators
- **Volume change**

Other Engineered Features
- Rolling mean & rolling volatility

These engineered features help the model understand **momentum, volatility, and reversal patterns** in the market.


Machine Learning Models Used

Random Forest Regressor
- Handles non-linear relationships well  
- Robust to noise  
- Achieved the best performance *(if true for your notebook)*

Linear Regression
- Baseline statistical model  
- Useful for benchmarking


Model Training & Workflow

1. Load historical NIFTY data  
2. Perform preprocessing (missing values, scaling, alignment)  
3. Generate technical indicators  
4. Create lag features  
5. Train-test split  
6. Train models (RF & LR)  
7. Evaluate using RMSE/MAE/R²  
8. Compare results  
9. Plot predictions vs actuals  

Results
- Random Forest Regressor performed better than Linear Regression  
- Feature importance showed strong signal for:  
  - EMAs  
  - RSI  
  - MACD  
  - Bollinger Band width  
  - ATR  
- The model captures short-term market patterns but remains sensitive to volatility spikes.

Technologies Used

- **Python**
- **pandas, NumPy**
- **scikit-learn**
- **matplotlib / seaborn**
- **yfinance**
  

Project Structure
├── stock_market_predictor.ipynb   # Main notebook (Colab)
├── README.md                      # Project documentation
├── data/                          # (Optional) Local saved datasets
└── plots/                         # (Optional) Visualizations
