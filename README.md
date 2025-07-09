![alt text](https://github.com/denisgaribovic/sales-forecasting/blob/main/Banner.png)

# 📈 Sales Forecasting

A production-ready time series forecasting pipeline built with [Meta Prophet](https://facebook.github.io/prophet/), designed to help retailers **optimize inventory, staffing, and promotional strategies**. This project demonstrates how daily sales can be forecasted using a mix of **historical transactions**, **external economic signals**, and **seasonal effects** — all in a modular, interpretable, and scalable workflow.

---

## ✨ Highlights

- 📆 Forecasted daily sales across 54 stores and multiple product families  
- 🌍 Integrated oil prices, national holidays, and store-level transactions as external regressors  
- ⚙️ Built a reusable forecasting pipeline using Prophet in Python  
- 📊 Evaluated accuracy using MAE and RMSE for business-ready insights  
- 🧩 Easily extendable to other retail or time series forecasting use cases  

---

## 🎯 Business Context

In fast-paced retail environments, poor sales forecasting leads to **stockouts**, **excess inventory**, and **inefficient staffing** — all of which hurt both revenue and customer satisfaction.  

This project enables retail teams to:

- 🛍️ Plan promotions and product availability more precisely  
- 🧾 Align staffing and procurement with expected sales demand  
- 📉 Respond to external signals like oil price trends and holiday seasonality  
- 📦 Improve supply chain and warehouse utilization  

---

## 🔐 Real-World Applications

This forecasting pipeline can be used or extended for:

- 🧮 Daily or weekly demand planning across locations  
- 🗓️ Promotion-aware forecasting for marketing campaigns  
- 🧠 Scenario modeling with dynamic holiday or economic inputs  
- 📊 Dashboard integrations for inventory and operations teams  

---

## 📚 Dataset Overview

The dataset originates from the [Kaggle Store Sales Time Series Forecasting competition](https://www.kaggle.com/competitions/store-sales-time-series-forecasting/data), featuring:

| Dataset | Description | Key Columns |
|---------|-------------|-------------|
| `train.csv` | Daily sales per store and product family | `date`, `store_nbr`, `family`, `sales` |
| `transactions.csv` | Store-level daily transaction counts | `date`, `store_nbr`, `transactions` |
| `oil.csv` | Daily oil price (economic signal) | `date`, `dcoilwtico` |
| `holidays_events.csv` | National and local holidays/events | `date`, `type`, `locale`, `locale_name` |
| `stores.csv` | Store metadata | `store_nbr`, `city`, `state`, `type`, `cluster` |

---

## 🛠️ Project Workflow

### 1. 📥 Data Integration & Cleaning

- Merged multi-source data (sales, oil, holidays, transactions, store metadata)  
- Handled missing values via forward fill and domain-aware imputation  
- Ensured join integrity and avoided data leakage  

### 2. 🔍 Exploratory Data Analysis

- Explored long-term sales trends, seasonal patterns, and anomalies  
- Analyzed holiday impacts and weekly seasonality  
- Validated data consistency across sources  

### 3. 🤖 Forecasting with Prophet

- Modeled daily sales using Prophet with the following regressors:  
  - 🛍️ Promotions  
  - 🛒 Transactions  
  - 🛢️ Oil prices  
  - 📅 Holidays  
- Enabled flexible forecasting by store and product family  
- Split data into training and testing based on a time-based cutoff  

### 4. 📈 Model Evaluation

- Evaluated predictions using:  
  - 📉 Mean Absolute Error (MAE)  
  - 📊 Root Mean Squared Error (RMSE)  
- Visualized actual vs. forecasted sales  
- Aggregated performance metrics at weekly/monthly levels for stakeholder clarity  

---

## 💡 Key Takeaways

- 🔮 Incorporating external regressors like holidays and oil prices enhances forecast accuracy  
- 🧱 Modular pipeline structure allows easy scaling to other stores or time series problems  
- 📊 Clear visualizations help bridge the gap between technical insights and business decisions  
- 🚀 Prophet is a powerful tool for real-world retail forecasting when combined with domain features  
