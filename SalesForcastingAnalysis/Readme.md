# 🛍️ Superstore Sales Forecasting & Analysis

## 📌 Project Overview

This project analyzes the **Superstore Sales Dataset** (from Kaggle) to understand historical sales performance and build forecasting models that can predict future sales.

The goal of this project is to:

- Clean and preprocess the dataset  
- Perform time series analysis  
- Build and evaluate forecasting models  
- Extract business insights and future sales predictions  

---

## 📂 Dataset

**Source:** Superstore Sales Dataset (Retail store sales data)  
🔗 https://www.kaggle.com/datasets/bhanupratapbiswas/superstore-sales/data

The dataset includes the following key information:

| Column | Description |
|--------|-------------|
| Order ID | Unique identifier for each order |
| Order Date | Date of the sale |
| Ship Date | Date the product shipped |
| Customer ID | Customer unique identifier |
| Segment | Customer segment |
| City / State | Location of sale |
| Region | Sales region |
| Category | Product category |
| Sub-Category | Product subcategory |
| Sales | Revenue from the sale |
| Quantity | Number of items sold |
| Discount | Discount applied |
| Profit | Profit from the sale |

---

## 🧹 Data Preprocessing

The following preprocessing steps were carried out:

1. **Loading the dataset**
2. **Converting date columns to `datetime` format**
3. **Sorting data by order date**
4. **Cleaning missing values and duplicates**
5. **Aggregating sales by month**
6. **Creating time-dependent features (Year, Month, Quarter)**

---

## 📊 Exploratory Data Analysis (EDA)

We performed:

- Line plots to visualize monthly sales trends
- Seasonal decomposition (trend, seasonality, residual)
- Sales distribution by category/region
- Correlation heatmap for numerical features

---

## 🛠 Feature Engineering

The following time-series based features were created:

| Feature | Source |
|---------|--------|
| Year | Order Date |
| Month | Order Date |
| Quarter | Order Date |
| Total Monthly Sales | Aggregated sales |

These features were used to build regression forecasting models.

---

## 🤖 Forecasting Models

### 🔹 Baseline Model: Moving Average  
Useful to capture short-term trends.

### 🔹 Linear Regression

- Used Year, Month, and Quarter as predictors
- Easy to interpret
- Often used for trend forecasting

### 🔹 Random Forest Regressor

- Captures non-linear trends
- Better forecasting performance
- Handles interactions between variables

---

## 📈 Model Evaluation Metrics

We used the following metrics:

| Metric | Description |
|--------|-------------|
| MAE | Mean Absolute Error |
| RMSE | Root Mean Squared Error |
| R² Score | Model fit accuracy |

Random Forest model generally performs better for forecasting non-linear sales patterns.

---

## 📈 Actual vs Forecast Visualization

We visualize how closely the predicted values match actual monthly sales:

```python
plt.figure(figsize=(12,6))
plt.plot(test['Order Date'], y_test, label='Actual')
plt.plot(test['Order Date'], y_pred_rf, label='Predicted')
plt.legend()
plt.title("Actual vs Predicted Sales")
plt.show()
```
---
## 🛠 Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib & Seaborn
- Scikit-learn
---
## 📦 Project Structure
```text
Superstore-Sales-Forecasting/
│
├── superstore_sales.csv
├── SalesForecastingAnalysis.ipynb
└── README.md
```

