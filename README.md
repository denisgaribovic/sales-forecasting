![alt text](https://github.com/denisgaribovic/sales-forecasting/blob/main/Banner.png)

# 📈 Sales Forecasting

A **data-driven sales forecasting pipeline** designed for retail leaders to optimize **inventory, promotions, and staffing**. This project uses [Meta Prophet](https://facebook.github.io/prophet/) and combines internal sales data with external signals like oil prices, holidays, and transactions to deliver **interpretable, accurate, and scalable daily forecasts** — ready for deployment across retail networks.

---

## ✨ Highlights

- 📆 Forecasts daily sales across 54 stores and multiple product families  
- 🌍 Incorporates oil prices, holidays, and transactions as external regressors  
- ⚙️ Modular pipeline built in Python using Prophet  
- 📊 Visual reports and KPIs (MAE, RMSE) for stakeholder-friendly evaluation  
- 🧩 Easily adaptable to other time series forecasting scenarios  

---

## 🎯 Business Context

In fast-moving retail environments, poor forecasting leads to **stockouts, waste, missed promotions, and unhappy customers**.  

This project empowers **retail planners, marketing teams, and supply chain leads** to:  
- Anticipate local sales surges and seasonality  
- Plan staffing and procurement more effectively  
- Respond to external factors such as holidays and oil price fluctuations  

---

## 🛠️ Project Workflow

The forecasting pipeline is modular, interpretable, and scalable. The main steps include:

### 1. 📥 Data Integration & Cleaning

- Merges sales data with external sources: oil prices, holidays, transactions, and store metadata  
- Handles missing values with forward-filling and sensible defaults  
- Ensures no data leakage or unintended row multiplication during joins  

### 2. 🔍 Exploratory Data Analysis

- Visualizes long-term trends, weekly seasonality, and holiday effects  
- Decomposes the time series into trend, seasonal, and residual components  
- Validates data quality and informs modeling choices  

### 3. 🤖 Forecasting with Prophet

- Forecasts daily sales with Prophet, including optional external regressors:  
  - 🛍️ Promotions  
  - 🛒 Transactions  
  - 🛢️ Oil prices  
  - 📅 Holiday indicators  
- Provides a flexible function to forecast for any store/product combination  
- Automatically splits data into training and testing sets based on a cutoff date  

### 4. 📈 Model Evaluation

- Calculates MAE and RMSE on the forecast horizon  
- Visualizes actual vs. predicted sales  
- Offers weekly and monthly aggregation views for stakeholder-friendly reporting
