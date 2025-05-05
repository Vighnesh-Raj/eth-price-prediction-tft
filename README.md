# Ethereum Price Prediction using Temporal Fusion Transformer (TFT)

This project applies a Temporal Fusion Transformer (TFT) to predict short-term price movements of Ethereum (ETH) using time-series deep learning techniques. It includes data preprocessing, feature engineering with technical indicators, model training using `pytorch-forecasting`, and backtesting of a simple trading strategy.

## 📌 Project Summary

- **Goal**: Forecast ETH/USD closing prices and evaluate a trading strategy based on predictions.
- **Model**: Temporal Fusion Transformer (TFT)
- **Data**: 4-hour OHLCV crypto data from Alpaca Crypto API
- **Features**:
  - Moving Averages (daily, weekly, monthly)
  - Rolling Volatility
  - Relative Strength Index (RSI)
  - BTC/ETH Rolling Correlation
- **Trading Strategy**:
  - Buy if predicted price ↑ > 1%
  - Sell if predicted price ↓ > 2%
  - Hold otherwise

## 📈 Results

- Final Portfolio Value: **$11,071.54** (starting from $10,000)
- Sharpe Ratio: **0.0158**
- Max Drawdown: **-76.43%**
- Strategy was conservative with ~96.5% Hold signals

## 📂 Files

- `notebook/ETH_TFT_Model_VR.ipynb` – Full model development notebook
- `results/ETH_TFT_Model_VR.html` – Static HTML version
- `results/Final_Presentation_VR.pdf` – Summary presentation

## ⚙️ Setup

Install required dependencies:

```bash
pip install -r requirements.txt
```

## 🧠 Author

Vighnesh Raj  
MS Business Analytics, University of Cincinnati  
[LinkedIn](https://www.linkedin.com/in/vighneshraj) • [Email](mailto:vighnesh_raj@live.com)