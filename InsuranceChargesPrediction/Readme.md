# 🏥 Medical Insurance Cost Analysis & Prediction

## 📌 Project Overview

This project analyzes the **Medical Cost Personal Dataset (Insurance Dataset)** from Kaggle to identify the key factors affecting medical insurance charges and build machine learning models to predict insurance costs.

The objective is to:
- Perform data cleaning and preprocessing
- Analyze relationships between variables
- Visualize trends and patterns
- Build predictive machine learning models
- Extract actionable business insights

---

## 📂 Dataset

The dataset contains the following features:

| Feature   | Description |
|----------|-------------|
| age | Age of primary beneficiary |
| sex | Gender (male/female) |
| bmi | Body Mass Index |
| children | Number of dependents |
| smoker | Smoking status (yes/no) |
| region | Residential region |
| charges | Medical insurance cost (target variable) |

---

## 🧹 Data Preprocessing

The following preprocessing steps were performed:
- Checked for missing values
- Removed duplicate records
- Handled categorical variables using:
  - Label Encoding (for correlation analysis)
  - One-Hot Encoding (for machine learning models)
- Feature scaling using StandardScaler for Linear Regression

---

## 📊 Exploratory Data Analysis (EDA)

We performed:
- Distribution analysis of insurance charges
- Scatter plots (Age vs Charges, BMI vs Charges)
- Box plots (Smoker vs Charges, Region vs Charges)
- Correlation heatmap
- Statistical correlation tests (Pearson correlation)

---

## 🔍 Key Insights from Analysis

- 🚬 Smoking status is the strongest factor influencing medical charges
- 📈 Age has a positive correlation with insurance cost
- ⚖️ Higher BMI slightly increases charges
- 🌍 Region has minimal impact on charges
- 👨‍👩‍👧 Number of children has low influence on insurance cost

---

## 🤖 Machine Learning Models

Two regression models were implemented:

### 1️⃣ Linear Regression
- Used StandardScaler
- R² Score ≈ 0.75–0.80
- Good baseline model

### 2️⃣ Random Forest Regressor
- 200 estimators
- No scaling required
- R² Score ≈ 0.85–0.90
- Better performance due to handling non-linear relationships

---

## 📈 Model Evaluation Metrics

The following metrics were used:
- MAE (Mean Absolute Error)
- RMSE (Root Mean Squared Error)
- R² Score (Model accuracy)

Random Forest outperformed Linear Regression in prediction accuracy and error reduction.

---

## 🧠 Feature Importance

Random Forest feature importance analysis revealed:
1. Smoker status (most influential)
2. Age
3. BMI
4. Number of children
5. Region (least impactful)

---

## 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- SciPy

---
