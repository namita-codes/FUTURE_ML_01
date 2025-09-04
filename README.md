# 📊 FUTURE_ML_01 - Walmart Retail Sales Forecasting

## 📌 Problem Statement
The goal of this project (Future Interns Task 1) is to **forecast Walmart’s weekly retail sales** using **time series forecasting**.  
Accurate sales forecasting helps businesses plan inventory, staffing, and marketing strategies effectively.

---

## 📂 Dataset
- **Source**: [Walmart Dataset on Kaggle](https://www.kaggle.com/datasets/yasserh/walmart-dataset)  
- **Columns**:
  - `Store` → Store ID  
  - `Dept` → Department ID  
  - `Date` → Week start date  
  - `Weekly_Sales` → Weekly sales revenue  

---

## 🔧 Approach
1. **Data Cleaning & Preprocessing**
   - Converted `Date` to datetime format  
   - Aggregated sales **per store per week**  
2. **Forecasting Model**
   - Used **Facebook Prophet** for time series forecasting  
   - Forecast horizon: **12 weeks**  
   - Evaluated with metrics: MAE, RMSE, MAPE  
3. **Visualization**
   - Plots generated for each store (`plots/`)  
   - Interactive dashboard built using **Plotly**  

---

## 📈 Results
- **Forecasts**:
  - Per-store forecasts → [`forecasts/store_X_forecast.csv`](forecasts/)  
  - Combined forecast for all stores → [`forecasts/all_stores_forecast.csv`](forecasts/all_stores_forecast.csv)  
- **Plots**:
  - Forecast plots → [`plots/store_X_forecast.png`](plots/)  
  - Prophet trend & seasonality → [`plots/store_X_components.png`](plots/)  
- **Metrics** (example: Store 1)
  ```json
  {
    "MAE": 12345.6,
    "RMSE": 23456.7,
    "MAPE": 12.3
  }
