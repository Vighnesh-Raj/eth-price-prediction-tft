# ETH Price Prediction using Temporal Fusion Transformer (TFT)

This project implements a deep learning-based time series forecasting model to predict Ethereum (ETH) prices using a Temporal Fusion Transformer (TFT). It combines technical indicators, market trends, and Bitcoin correlation features to generate actionable trading signals.

## 🧠 Author
Vighnesh Raj  
MS Business Analytics, University of Cincinnati  
📧 vighnesh_raj@live.com

## 📈 Problem Statement

Predict short-term future ETH/USD price movements using a combination of crypto market data and engineered features, and use those forecasts to simulate a trading strategy.

## 🧠 Model: Temporal Fusion Transformer (TFT)

The TFT model from `pytorch-forecasting` is used for multivariate time-series forecasting. It captures both short- and long-term dependencies using attention mechanisms and recurrent layers (GRU).

## 🛠 Features Engineered
- Resampled 4-hour interval OHLCV data from Alpaca Crypto API (BTC/USD & ETH/USD)
- Technical indicators:
  - Moving Averages (daily, weekly, monthly)
  - Volatility (rolling std)
  - RSI for ETH
  - BTC-ETH rolling correlation

## ⚙️ Model Parameters
- Hidden size: 128
- Attention heads: 4
- Epochs: 100 (with early stopping)
- Loss: Mean Squared Error (MSE)

## 📊 Backtesting Strategy
- **Buy**: Predicted ETH price increases by >1%
- **Sell**: Predicted price drops by >2%
- **Hold**: Otherwise

## 💼 Results
- Final Portfolio Value: `$11,071.54` (from initial $10,000)
- Sharpe Ratio: 0.0158
- Max Drawdown: -76.43%
- Most signals were conservative (96.5% Hold)

## 📂 Files
- `ETH_TFT_Model_VR.html`: Full model output and visualizations
- `Final_Presentation_VR.pdf`: Slide deck summarizing the approach and findings

## 🔧 Future Work
- Add macroeconomic and sentiment data
- Improve risk-adjusted returns with better position sizing and stop-loss logic
- Experiment with alternative time series models (e.g., N-BEATS, TCN)
