# 📈 Apple Stock Price Prediction using KNN

This project leverages the **K-Nearest Neighbors (KNN)** algorithm to perform both **classification** (price up/down) and **regression** (predicting actual closing price) on **Apple Inc. (AAPL)** stock data over a 10-year period.

## 📦 Dataset
- **Source**: [Yahoo Finance](https://finance.yahoo.com/)
- **Ticker**: `AAPL`
- **Time Period**: `2014-01-01` to `2024-01-01`
- Data collected using the `yfinance` API.

## 🧪 Libraries Used
- `pandas`, `numpy` for data manipulation
- `matplotlib` for data visualization
- `yfinance` for stock data extraction
- `sklearn` for machine learning models and evaluation

## 💡 Features Created
From the raw stock data, we derived:
- `Open - Close`: Difference between opening and closing price
- `High - Low`: Daily price volatility

These features were used for both classification and regression models.

---

## 🔍 1. Classification Task
**Objective**: Predict whether the next day's closing price will be higher (`1`) or lower (`-1`) than the current day's close.

### ✅ Model
- **Algorithm**: K-Nearest Neighbors (`KNeighborsClassifier`)
- **Tuning**: Used `GridSearchCV` to find the optimal number of neighbors (k)
- **Train-Test Split**: 75-25

### 📊 Accuracy
```text
Train Accuracy: 0.61
Test Accuracy:  0.52
```
📋 Sample Output
| Actual | Predicted |
| ------ | --------- |
| 1      | 1         |
| -1     | 1         |
| 1      | 1         |

## 🔁 2. Regression Task
**Objective:** Predict the actual closing price of AAPL stock.

### ✅ Model
**Algorithm:** K-Nearest Neighbors (KNeighborsRegressor)
**Tuning:** Used GridSearchCV to optimize n_neighbors

### 📉 Evaluation Metric
Root Mean Squared Error (RMSE) was used to assess performance:
```text
RMSE: ~93.12
```
📋 Sample Output
| Actual Close | Predicted Close |
| ------------ | --------------- |
| 145.62       | 146.01          |
| 150.22       | 149.84          |

## 📈 Visualizations
Line plot of AAPL’s closing price history from 2014 to 2024.
(Optional) You can further enhance the repo with:
Confusion matrix for classification
Error plot for regression

▶️ How to Run
1. Install dependencies:
```bash
pip install pandas numpy matplotlib yfinance scikit-learn
```
2. Run the Python script or Jupyter notebook

## 🛠️ Future Improvements
Use additional technical indicators like RSI, MACD, Moving Averages
Try other models: Random Forest, SVM, LSTM
Add backtesting functionality
