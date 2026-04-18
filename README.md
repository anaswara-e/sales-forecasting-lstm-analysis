# 📊 Sales Forecasting using LSTM with Feature Impact Analysis.

## 🚀 Overview
This project focuses on forecasting retail sales using Deep Learning (LSTM) and analyzing model behavior under different feature configurations.

Instead of only building a model, this project explores:
- How LSTM performs on time-series data
- Impact of feature selection on prediction accuracy
- Comparison with a simple baseline model

---

## 🎯 Problem Statement
Predict daily retail sales using historical data and evaluate:

- Whether temporal patterns alone are sufficient for prediction
- How external business factors (e.g., promotions, customers) influence performance
- Whether deep learning models outperform traditional approaches

---

## 📂 Dataset
The dataset is not included in this repository due to size constraints.

You can download it from:
https://www.kaggle.com/competitions/rossmann-store-sales/data

### Dataset includes:
- ~800K+ retail store records
- Features:
  - Date (Day, Month, Weekday)
  - Sales
  - Promo
  - Customers

---

## ⚙️ Approach

### 1. Data Preprocessing
- Converted date column to datetime format  
- Removed closed stores and invalid sales values  
- Handled outliers using quantile-based filtering  
- Feature engineering:
  - Day, Month, Weekday extracted from Date  

---

### 2. Time-Series Preparation
- Scaled features using MinMaxScaler  
- Created sequential input data for LSTM  
- Sequence length: 30 time steps  

---

### 3. Model Building (LSTM)
- Built a stacked LSTM architecture using TensorFlow/Keras  
- Used Dropout to reduce overfitting  
- Loss function: Mean Squared Error (MSE)  
- Optimizer: Adam  

---

### 4. Baseline Model
- Linear Regression model used as a baseline for comparison  

---

### 5. Experiment Setup
This project evaluates model behavior under different feature conditions:

- Full feature set (Sales + Promo + Customers + Date features)
- Reduced feature set (Time-series patterns only)

---

## 📊 Results

| Model                          | RMSE |
|--------------------------------|------|
| Linear Regression (Baseline)   | 2375 |
| LSTM (Time-Series Only)        | 2122 |

👉 LSTM improved performance over baseline when modeling temporal patterns, but still struggles with high volatility in sales data.

---

## 📈 Visualizations

### 🔹 Actual vs Predicted Sales
- LSTM captures overall trends and seasonality  
- Struggles with sudden spikes in sales  

### 🔹 Training vs Validation Loss
- Stable convergence observed  
- Slight underfitting indicates model limitations  

---

## 🧠 Key Insights

- LSTM performs better when learning temporal patterns  
- Removing external features improves sequence learning but reduces real-world accuracy  
- Business variables like promotions and customer count significantly impact predictions  
- Feature engineering plays a critical role in model performance  

---

## ⚠️ Observations

- Predictions are smoother than actual values  
- Model struggles to capture high volatility in sales  
- Indicates potential suitability of tree-based models for structured tabular data  

---

## 🛠️ Tech Stack

- Python  
- Pandas, NumPy  
- Scikit-learn  
- TensorFlow / Keras  
- Matplotlib  

---

## 📁 Repository Structure
├── lstm_analysis.ipynb
├── lstm_model.keras
├── Prediction Plot.png
├── Loss Curve Plot.png
├── requirements.txt
├── README.md

---


---

## 🚀 Future Improvements

- Compare with Random Forest and XGBoost models  
- Improve LSTM architecture (GRU, Attention mechanisms)  
- Feature selection optimization  
- Hyperparameter tuning for better generalization  

---

## 💡 Conclusion

This project demonstrates that:

> Model performance in real-world problems depends heavily on feature selection, not just model complexity.

LSTM effectively captures temporal patterns, but external business features are crucial for accurate sales forecasting.

---

## 🔗 Author

**Anaswara E**

- LinkedIn: https://www.linkedin.com/in/anaswara-e  
- GitHub: https://github.com/anaswara-e  
