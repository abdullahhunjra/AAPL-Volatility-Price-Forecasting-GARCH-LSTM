# 📊 AAPL Stock Risk & Price Forecasting using GARCH & LSTM

This project explores **risk forecasting** and **price prediction** for Apple Inc. (AAPL) using both **traditional statistical models** (GARCH, ARCH family) and **deep learning (LSTM)**.

---

## 🎯 Project Objective

- Forecast **volatility (risk)** in AAPL stock using GARCH-type models.
- Predict **future prices** using LSTM neural networks.
- Compare how well statistical vs. deep learning models perform under different market conditions.
- Build interpretable visuals to show model forecasts and real-world context (e.g., geopolitical shocks).

---

## 🧭 Project Workflow

| Phase | Task |
|-------|------|
| ✅ 1 | Data Collection via Yahoo Finance (2020–2025) |
| ✅ 2 | Log Returns + Rolling Volatility Computation |
| ✅ 3 | GARCH-t Volatility Modeling (1-day ahead forecasts) |
| ✅ 4 | Value at Risk (VaR) Estimation |
| ✅ 5 | LSTM Price Forecasting with Feature Engineering |
| ✅ 6 | Rolling Window Forecasts + Visual Comparison |
| ✅ 7 | Final Evaluation: RMSE, MAE, MAPE, R² |
| ✅ 8 | Interpretations + Visual Explanations |
| ✅ 9 | README + GitHub polish |

---

## 📚 Models & Tools Used

| Tool / Model       | Purpose                                      |
|--------------------|----------------------------------------------|
| `arch` (GARCH-t)   | Volatility Forecasting                       |
| `tensorflow.keras` | LSTM Neural Network Modeling                 |
| `matplotlib`/`seaborn` | Clean Visualizations                      |
| `yfinance`         | Data Sourcing                                |

---

## 📈 Volatility Forecasting (GARCH-t)

We used a **GARCH(1,1)** model with a **Student-t distribution** to capture heavy tails in returns. Forecasts were validated against **realized 30-day volatility**.

A major volatility spike in **April 2025** was accurately captured by the model, coinciding with **President Trump’s global tariff announcement**, which caused a sudden market crash and surge in investor fear.

📉 GARCH-t Highlights:
- Captures volatility clustering well
- Responds quickly to shocks
- Used to estimate **Value at Risk (VaR)**

---

## 🤖 Price Forecasting (LSTM)

We trained an LSTM model using:
- Lookback window of 90 days
- Normalized price sequences
- Forecast horizon of 30 days


📉 LSTM Evaluation Metrics:
- **RMSE:** ~$3.92  
- **MAE:** ~$2.77  
- **R² Score:** ~0.60  
- **MAPE:** ~1.37%

Despite volatile markets, the LSTM handled future prediction impressively well.

---

## 🧠 Why Two Data Horizons?

We used different timeframes for different model types:

| Model Type | Dataset Span | Reason |
|------------|--------------|--------|
| GARCH-t (Volatility) | 2024–2025 | Sensitive to recent shocks |
| LSTM (Price)         | 2020–2025 | Needs large dataset to learn patterns |

Keeping short- and long-span data **modular and separate** improved both interpretability and model performance.

## 👨‍💻 Author

**Abdullah Shahzad**  
📧 Email: [abdullahshahzadhunjra@gmail.com](mailto:abdullahshahzadhunjra@gmail.com)  
🔗 GitHub: [github.com/abdullahhunjra](https://github.com/abdullahhunjra)  
🔗 LinkedIn: [linkedin.com/in/abdullahhunjra](https://linkedin.com/in/abdullahhunjra)


## 📦 Folder Structure

