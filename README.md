# 📊 Sales Forecasting using LSTM with Feature Impact Analysis

## 🚀 Overview
This project focuses on forecasting retail sales using Deep Learning (LSTM) and analyzing how **feature selection impacts model performance**.

Instead of only building a model, this project explores:
- When LSTM works well
- When traditional models perform better
- How business features affect predictions

---

## 🎯 Problem Statement
Predict daily sales using historical data and evaluate whether:
- Temporal patterns alone are sufficient, or
- External business features (e.g., promotions, customers) improve performance

---

## 📂 Dataset
- ~800K+ records of retail store sales  
- Features include:
  - Date (Day, Month, Weekday)
  - Sales
  - Promo
  - Customers  

---

## ⚙️ Approach

### 1. Data Preprocessing
- Converted date to datetime format  
- Removed closed stores and zero sales  
- Handled outliers using quantile filtering  
- Feature engineering:
  - Day, Month, Weekday  

---

### 2. Time-Series Preparation
- Normalized features using MinMaxScaler  
- Created sequences of past observations  
- Sequence length: **30 days**

---

### 3. Model Building (LSTM)
- Two-layer LSTM architecture  
- Dropout used to reduce overfitting  
- Trained using Mean Squared Error loss  

---

### 4. Experiment: Feature Impact Analysis

Two setups were tested:

#### 🔹 Model A: Full Features
- Sales + Promo + Customers + Date features  

#### 🔹 Model B: Time-Series Only
- Sales + Date features only  

---

### 5. Baseline Model
- Linear Regression used as baseline for comparison  

---

## 📊 Results

| Model                          | RMSE |
|--------------------------------|------|
| Linear Regression (Baseline)   | 2375 |
| LSTM (Time-Series Only)        | 2122 |

---

## 📈 Visualizations

### 🔹 Actual vs Predicted Sales
- LSTM captures overall trends and seasonality  
- Struggles with extreme spikes  

### 🔹 Training vs Validation Loss
- Stable curves indicate no severe overfitting  
- Slight underfitting observed  

---

## 🧠 Key Insights

- LSTM performs better when modeling **pure temporal patterns**
- Removing business features reduces ability to capture real-world variability  
- External factors (Promo, Customers) play a critical role in prediction  
- Model performance depends heavily on **feature selection**, not just model choice  

---

## ⚠️ Observations

- LSTM predictions are smoother and miss sharp spikes  
- Indicates difficulty in capturing high variability  
- Suggests that:
  - Tree-based models may perform better for structured tabular data  

---

## 🛠️ Tech Stack

- Python  
- Pandas, NumPy  
- Scikit-learn  
- TensorFlow / Keras  
- Matplotlib  

---

## 📁 Project Structure
├── notebook/
│ └── lstm_analysis.ipynb
├── model/
│ └── lstm_model.keras
├── images/
│ ├── prediction_plot.png
│ └── loss_plot.png
├── README.md


---

## 🚀 Future Improvements

- Try tree-based models (Random Forest, XGBoost) for comparison  
- Hyperparameter tuning for LSTM  
- Incorporate more business features  
- Use advanced architectures (GRU, Attention)  

---

## 💡 Conclusion

This project demonstrates that:
> Choosing the right features is as important as choosing the right model.

While LSTM is powerful for time-series data, combining **temporal patterns with domain-specific features** is essential for accurate predictions.

---

## 🔗 Author

**Anaswara E**  
- LinkedIn: https://www.linkedin.com/in/anaswara-e  
- GitHub: https://github.com/anaswara-e  

