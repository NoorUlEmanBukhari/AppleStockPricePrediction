## Apple Stock Price Prediction using LSTM

This project focuses on predicting **Apple Inc. (AAPL)** stock prices using a Long Short-Term Memory (LSTM) model. It aims to forecast the next day's **closing price** using historical stock data and evaluate how well LSTM handles stock market trends, volatility, and multi-step forecasting.

---

## 📊 Dataset

- **Source**: Apple stock data (CSV file)
- **Timeframe**: Includes daily trading data with columns:
  - `Date`, `Open`, `High`, `Low`, `Close`, `Adj Close`, `Volume`
- **Preprocessing Steps**:
  - Converted `Date` to datetime and set as index
  - Focused on the `Close` price for prediction
  - Scaled data using `MinMaxScaler`
  - Created sequences (windowed input) for LSTM model

---

## 🔍 Objective

- Build a deep learning model to predict the **next day’s closing price**.
- Evaluate LSTM’s capability for time series forecasting.
- Observe its behavior in **multi-step forecasting** (where it struggled).
- Identify areas for improvement using more advanced models.

---

## 🧠 Model Architecture

### ✅ LSTM Model

- Framework: TensorFlow / Keras
- Architecture:
  - One LSTM layer
  - Dense output layer for prediction
- Input: Past `n` days of closing prices
- Output: Next day's closing price
- Loss: Mean Squared Error (MSE)
- Optimizer: Adam

---

## 📈 Results

### ✅ Single-step prediction:
- Performs well with low error
- Captures short-term trends

### ❌ Multi-step prediction:
- Model repeatedly predicts a **downtrend**
- Fails to generalize in volatile price movements
- Struggles with larger price ranges

### 📉 Evaluation Metrics:
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- Plots of Actual vs Predicted Prices

---

## 📌 Key Observations

| Aspect                  | Result |
|-------------------------|--------|
| One-day prediction      |  Accurate |
| Multi-day forecasting   |  Poor performance |
| Price volatility        |  LSTM struggled |
| Trend reversal detection|  Weak response |

---

## 🔄 Future Work

- 🔁 Implement **Seq2Seq** for improved sequence prediction
- ⚙️ Try **Transformer**-based models with attention
- ➕ Include **technical indicators** (e.g., RSI, MACD) as features
- 📈 Train on longer history for better context
- 💻 Optionally deploy via Streamlit for live testing

---

## 🛠 Tools & Libraries

- Python
- Jupyter Notebook
- TensorFlow / Keras
- NumPy
- Pandas
- Matplotlib, Seaborn
- Scikit-learn

---


