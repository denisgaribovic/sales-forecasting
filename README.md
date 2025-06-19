![alt text](https://github.com/denisgaribovic/sales-forecasting/blob/main/Banner.png)

This project builds a production-ready forecasting pipeline to predict **daily retail sales** using [Meta Prophet](https://facebook.github.io/prophet/). It combines historical sales with contextual data such as oil prices, holidays, transactions, and store metadata to improve forecast accuracy and business relevance.

## 🎯 Business Context

Retailers must balance **inventory planning**, **promotion timing**, and **staffing needs** across thousands of products and store locations. Manual forecasting is time-consuming and often fails to capture seasonal trends or external influences.

This project solves that problem by delivering an **automated, flexible, and accurate forecasting model** that can be used to:

- Optimize inventory and avoid stockouts or overstocking  
- Align promotional efforts and staffing with demand  
- Support supply chain and procurement decisions  
- Increase operational efficiency and customer satisfaction  

## 🛠️ Project Workflow

The forecasting pipeline is built to be modular, interpretable, and scalable. Here's what it does:

### 1. 📥 Data Integration & Cleaning
- Merges sales data with external sources: oil prices, holidays, transactions, store info  
- Handles missing values with forward-filling and defaulting  
- Ensures no row multiplication or data leakage during joins  

### 2. 🔍 Exploratory Data Analysis
- Visualizes long-term trends, weekly seasonality, and holiday effects  
- Decomposes time series into trend, seasonality, and residuals  
- Confirms data quality and guides modeling strategy  

### 3. 🤖 Forecasting with Prophet
- Forecasts daily sales using Prophet with optional external regressors:
  - 🛍️ Promotions  
  - 🛒 Transactions  
  - 🛢️ Oil prices  
  - 📅 Holiday indicators  
- Includes a flexible function to forecast for any store/product combination  
- Automatically splits training/testing data using a cutoff date  

### 4. 📈 Model Evaluation
- Calculates MAE and RMSE on the forecasted period  
- Visualizes actual vs. predicted sales  
- Weekly and monthly aggregations available for stakeholder-friendly reporting 

## 📊 Dataset Overview

This project uses data from the [Kaggle Store Sales - Time Series Forecasting competition](https://www.kaggle.com/competitions/store-sales-time-series-forecasting/data), featuring:

| Dataset             | Description                                                     |
|---------------------|-----------------------------------------------------------------|
| `train.csv`         | Daily sales per store/product family                            |
| `stores.csv`        | Store metadata: location, cluster, type                         |
| `oil.csv`           | Daily Ecuadorian oil prices                                     |
| `holidays_events.csv` | National and local holidays/events                             |
| `transactions.csv`  | Daily transaction count per store                               |

## 💡 Business Impact

✅ Enables automatic forecasts for any store or product  
✅ Supports demand planning, inventory management, and promotional strategy  
✅ Saves manual effort and enhances decision-making accuracy  
✅ Ready to scale across multiple retail locations and product hierarchies  
