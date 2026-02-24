# 🏠 Boston House Price Prediction using Linear Regression

## 📌 Project Overview

This project implements a **House Price Prediction model** using the classic **Boston Housing Dataset**. The objective is to build a regression model that predicts house prices based on various socio-economic and structural features.

The project demonstrates:

- Loading dataset using Scikit-learn
- Data preparation and type conversion
- Train-test splitting
- Building a Linear Regression model
- Evaluating model performance using multiple metrics
- Comparing actual vs predicted prices

---

## 📂 Dataset Information

The dataset used is the **Boston Housing Dataset**, loaded using `fetch_openml` from Scikit-learn.

It contains 506 observations with 13 features describing housing characteristics.

### 🔎 Features Include:

| Feature | Description |
|----------|-------------|
| CRIM | Per capita crime rate by town |
| ZN | Proportion of residential land zoned |
| INDUS | Proportion of non-retail business acres |
| CHAS | Charles River dummy variable |
| NOX | Nitric oxide concentration |
| RM | Average number of rooms per dwelling |
| AGE | Proportion of owner-occupied units built prior to 1940 |
| DIS | Distance to employment centers |
| RAD | Index of accessibility to highways |
| TAX | Property tax rate |
| PTRATIO | Pupil-teacher ratio |
| B | Proportion related to racial demographics |
| LSTAT | % Lower status of the population |
| Price | Median value of owner-occupied homes (Target Variable) |

---

## 🧹 Data Preparation

The following preprocessing steps were performed:

- Dataset loaded using `fetch_openml`
- Converted all feature columns to float
- Separated features (X) and target variable (y)
- Performed train-test split (80% training, 20% testing)
- Used `random_state=2` for reproducibility

---

## 🤖 Machine Learning Model

### ✅ Linear Regression

A Linear Regression model was implemented using Scikit-learn:

- Model trained on training dataset
- Predictions made on test dataset
- Model evaluated using multiple performance metrics

---

## 📊 Model Evaluation Metrics

The following evaluation metrics were used:

- **R² Score** – Measures how well the model explains variance
- **Mean Absolute Error (MAE)** – Average absolute difference between actual and predicted values
- **Mean Squared Error (MSE)** – Penalizes larger errors more strongly
- **Mean Squared Log Error (MSLE)** – Measures relative prediction error
## 📈 Results Interpretation

- The model achieves a reasonably strong R² score (~0.70–0.80).
- Linear Regression performs well but may not capture complex non-linear relationships.
- Features like average number of rooms (RM) and lower status percentage (LSTAT) typically show strong influence on price.
---
## 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

## 📦 Project Structure
```text
House-Price-Prediction/
│
├── HousePricePrediction.ipynb
├── README.md
└── BostonHousing.csv
