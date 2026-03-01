# SLU Opportunity Application Forecasting  
## Week 3 – Predictive Modeling & Forecast Insights Report  

### 👤 Author  
Zakhir Shaikh  

### 🏢 Internship Program  
Excelerate Internship Program  

---

# 📖 Project Overview  

This project focuses on building and evaluating machine learning models to forecast monthly application counts using historical SLU opportunity data.  

The goal is to develop a regression-based predictive model capable of estimating future application volumes to support strategic planning and operational decision-making.

---

# 🎯 Problem Statement  

Accurate forecasting of application counts is essential for resource allocation, capacity planning, and data-driven outreach strategies.  

This project implements regression models to predict future application trends based on historical temporal data.

---

# 📂 Dataset  

The dataset used in this project is the cleaned SLU Opportunity dataset prepared during Week 1 of the internship.  

It contains historical learner application records with time-based features used for forecasting.

---

# 🛠️ Data Preparation  

The following preprocessing steps were performed:

- Converted `Apply Date` to datetime format  
- Aggregated application counts at monthly level  
- Created a numerical `Time_Index` feature  
- Extracted `Month` and `Year` features  
- Applied chronological 80-20 train-test split  

Total historical period used: **34 months**

---

# 🤖 Machine Learning Models Implemented  

## 1️⃣ Linear Regression  
- Used as baseline model  
- Captures overall linear trend  

## 2️⃣ Random Forest Regressor  
- Ensemble learning model  
- Captures non-linear variations  
- Selected as final model  

---

# 📊 Model Evaluation Metrics  

Models were evaluated using:

- MAE (Mean Absolute Error)  
- RMSE (Root Mean Squared Error)  
- R² Score  

### 🔹 Linear Regression Results  
- MAE: 512.97  
- RMSE: 514.94  
- R²: -184.48  

### 🔹 Random Forest Results  
- MAE: 159.43  
- RMSE: 168.84  
- R²: -18.94  

Random Forest significantly reduced prediction error compared to the baseline model and was selected as the final forecasting approach.

---

# 🔮 Forecasting Output  

The final Random Forest model was used to:

- Generate test predictions  
- Compare actual vs predicted values  
- Forecast future 6-month application counts  

The forecast provides insight into expected application trends and supports proactive planning.

---

# 💡 Key Insights  

- Application trends show high month-to-month variability.  
- Non-linear behavior makes ensemble models more suitable.  
- Temporal features significantly influence application patterns.  

---

# 📈 Strategic Recommendations  

- Maintain flexible operational capacity due to forecast volatility.  
- Use predicted low-volume months for targeted outreach.  
- Re-train model periodically as new data becomes available.  

---

# ⚠️ Model Limitations  

- Limited to 34 months of historical data  
- External factors not included  
- Forecast assumes continuation of past trends  

Future improvements may include incorporating external variables and advanced time-series models.

---

# 🚀 How to Run the Project  

1. Clone this repository  
2. Install required libraries:
   ```bash
   pip install pandas numpy scikit-learn matplotlib
