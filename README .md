# 📈 Stock Price Prediction using LSTM (Deep Learning)

## 🚀 Project Overview

This project implements a Stock Price Prediction System using a Long
Short-Term Memory (LSTM) neural network. The model is trained on
historical stock market data to forecast the next day's closing price
based on the previous 60 days of closing prices.

The project demonstrates how deep learning models capture temporal
dependencies in time-series financial data.

------------------------------------------------------------------------

## 📊 Dataset Description

The dataset contains historical stock market data with the following
features:

-   Date -- Trading date
-   Open -- Opening price
-   High -- Highest price of the day
-   Low -- Lowest price of the day
-   Close -- Closing price
-   Adj Close -- Adjusted closing price
-   Volume -- Number of shares traded

------------------------------------------------------------------------

## 🧠 Problem Statement

To build a deep learning model that predicts the next day's stock
closing price using historical time-series data.

Since stock prices are sequential in nature, a recurrent neural network
approach (LSTM) is used to capture long-term dependencies and trends.

------------------------------------------------------------------------

## 🏗️ Methodology

### 1️⃣ Data Preprocessing

-   Converted Date column into datetime format
-   Selected Close price for prediction
-   Applied MinMax Scaling (0--1 normalization)

### 2️⃣ Sequence Generation

-   Look-back window = 60 days
-   Previous 60 days → Predict next day
-   Converted time-series into supervised learning format

### 3️⃣ Train-Test Split

-   80% Training data
-   20% Testing data
-   Maintained chronological order (no shuffling)

### 4️⃣ Model Architecture

-   LSTM Layer (50 units, return_sequences=True)
-   Dropout (0.2)
-   LSTM Layer (50 units)
-   Dropout (0.2)
-   Dense Layer (1 neuron output)

Optimizer: Adam\
Loss Function: Mean Squared Error (MSE)

------------------------------------------------------------------------

## 📐 Model Evaluation

The model was evaluated using:

-   RMSE (Root Mean Squared Error)
-   Percentage accuracy within 5% tolerance

Predictions were inverse-scaled back to original price values before
evaluation.

------------------------------------------------------------------------

## 🛠️ Technologies Used

-   Python
-   NumPy
-   Pandas
-   Matplotlib
-   Scikit-learn
-   TensorFlow / Keras

------------------------------------------------------------------------

## 📂 Project Structure

Stock-Price-Prediction/ │ ├── stock_data.csv ├──
stock_prediction_lstm.ipynb ├── stock_prediction_lstm.py ├── README.md

------------------------------------------------------------------------

## 🚀 Future Improvements

-   Add technical indicators (RSI, EMA, MACD)
-   Compare LSTM with GRU and ANN
-   Multi-feature prediction
-   Hyperparameter tuning
-   Deploy using Streamlit

------------------------------------------------------------------------

## 👨‍💻 Author

Gandra Bharadhwaj\
Artificial Intelligence & Machine Learning Student
