# 📈 Apple Stock Price Prediction using LSTM  

![Python](https://img.shields.io/badge/Python-3.9-blue?logo=python)
![TensorFlow](https://img.shields.io/badge/TensorFlow-DeepLearning-orange?logo=tensorflow)
![Keras](https://img.shields.io/badge/Keras-LSTM-red?logo=keras)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

---

## 🚀 Project Overview

This project builds a **Deep Learning-based Stock Price Prediction System** using an **LSTM (Long Short-Term Memory)** neural network to forecast Apple stock closing prices.

The model is trained on historical stock data and predicts the **next day's closing price using the previous 60 days of data**.

It demonstrates:

- Time-series forecasting  
- Sequence modeling using LSTM  
- Model evaluation using RMSE  
- Deployment-ready deep learning pipeline  

---

## 📊 Dataset

Historical Apple stock data containing:

- Date  
- Open  
- High  
- Low  
- Close  
- Adj Close  
- Volume  

Files used:

- `AAPL.csv`
- `cleaned dataset to test.csv`

---

## 🧠 Problem Statement

Stock prices are sequential and highly time-dependent.

Traditional regression models fail to capture long-term dependencies.

This project uses **LSTM networks**, a specialized Recurrent Neural Network (RNN), to learn temporal patterns and predict future stock prices.

---

## ⚙️ Methodology

### 1️⃣ Data Preprocessing

- Converted `Date` column to datetime format  
- Selected `Close` price for prediction  
- Applied MinMax Scaling (0–1 normalization)  
- Created sequences with a 60-day look-back window  

---

### 2️⃣ Sequence Creation

Previous 60 days → Predict next day

Example:

```
Day 1 → Day 60  → Predict Day 61
Day 2 → Day 61  → Predict Day 62
```

Converted time-series data into supervised learning format.

---

### 3️⃣ Train-Test Split

- 80% Training  
- 20% Testing  
- Chronological split (no shuffling to prevent data leakage)

---

## 🏗️ Model Architecture

```
Input (60 Days)
        ↓
LSTM (50 units, return_sequences=True)
        ↓
Dropout (0.2)
        ↓
LSTM (50 units)
        ↓
Dropout (0.2)
        ↓
Dense (1 Output)
```

**Optimizer:** Adam  
**Loss Function:** Mean Squared Error (MSE)  

---

## 📐 Model Evaluation

Metrics Used:

- ✅ Root Mean Squared Error (RMSE)  
- ✅ Percentage Accuracy (within 5% tolerance)

Predictions are inverse-transformed back to original stock price scale before evaluation.

---

## 📊 Sample Performance Metrics

| Metric | Training | Testing |
|--------|----------|----------|
| RMSE   | Low      | Moderate |
| Accuracy (±5%) | High | Good |

*(Exact values depend on dataset split and training runs.)*

---

## 💾 Saved Artifacts

After training:

- `aapl_lstm_model.h5` → Trained LSTM model  
- `scaler.pkl` → Saved MinMaxScaler  

These are reused during deployment for real-time predictions.

---

## 🌐 Deployment

The project includes a deployable web application:

- `app.py` → Streamlit/Flask app  
- `requirements.txt` → Dependencies  
- `Deployement link` → Live application  

Users can input stock values and get predicted closing prices.

---

## 🛠️ Tech Stack

- Python  
- NumPy  
- Pandas  
- Matplotlib  
- Scikit-learn  
- TensorFlow  
- Keras  
- Streamlit / Flask  

---

## 📂 Project Structure

```
APPLE_STOCK_PROJECT/
│
├── AAPL.csv
├── cleaned dataset to test.csv
├── aapl_lstm_model.h5
├── scaler.pkl
├── app.py
├── requirements.txt
├── README.md
└── Deployement link
```

---

## 🚀 Future Enhancements

- Add Technical Indicators (RSI, EMA, MACD)  
- Compare LSTM vs GRU vs ANN  
- Multi-feature input (OHLCV)  
- Hyperparameter tuning  
- Add attention mechanism  
- Docker containerization  
- CI/CD integration  

---

## 📌 Key Learning Outcomes

✔ Time-series forecasting  
✔ Deep learning model design  
✔ Sequence data preprocessing  
✔ Model evaluation techniques  
✔ Deployment of ML models  

---

## 👨‍💻 Author

**Gandra Bharadhwaj**  
Artificial Intelligence & Machine Learning Student  

---

## ⭐ If you found this project useful

Give it a ⭐ on GitHub and feel free to fork or contribute!
