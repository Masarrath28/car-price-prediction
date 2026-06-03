# car-price-prediction

# 🚗 Car Price Prediction 

Welcome to the Audi Car Price Prediction project repository! This project focuses on building an end-to-end Machine Learning pipeline to predict the prices of used Audi cars based on features like model, year, mileage, fuel type, engine size, and transmission.

A heavy emphasis is placed on comprehensive Exploratory Data Analysis (EDA) using NumPy, Pandas, Matplotlib, and Seaborn, followed by rigorous data preprocessing and regression model evaluation.

---

## 📊 Dataset Overview

The analysis is performed on the `audi.csv` dataset, which contains historical listings of Audi cars.

* Dataset Dimensions:  The dataset contains **10,668 records** and **9 distinct features** including the target variable price.
* Target Variable: `price`

---

## 🛠️ Tech Stack & Libraries Used

The project is implemented in Python utilizing the following core data science and machine learning libraries:

* 🐼 Pandas — Data manipulation, ingestion, structural cleaning, and slicing.
* 🔢 NumPy — Vectorized mathematical operations and array transformations.
* 📊 Matplotlib & Seaborn — Advanced statistical data visualizations, correlation heatmaps, and outlier detection.
* 🤖 Scikit-Learn — Feature scaling, encoding, data splitting, and classical regression models.
* 🚀 XGBoost — Gradient boosted decision trees for state-of-the-art predictive accuracy.

---

## 📈 Project Workflow & Methodology

### 1. Exploratory Data Analysis (EDA)
A deep-dive analysis was performed by comparing the target variable price against all independent variables to capture underlying trends and patterns:
* Visualized structural distributions and price ranges across different car models and years.
* Analyzed the negative correlation between mileage and price.
* Plotted categorical impacts such as transmission type and fuelType on overall price distribution.

### 2. Data Preprocessing & Feature Engineering
* **Categorical Encoding:** Leveraged LabelEncoder from Scikit-Learn to convert non-numeric categorical variables like `model`, `transmission`, `fuelType` into structured numerical representations.
* **Feature Scaling:** Applied StandardScaler from Scikit-Learn to standardize the features in the dataset, ensuring a uniform scale across features before training.
* **Data Splitting:** Divided the dataset into training and testing sets with an **80/20 split** (`test_size=0.2`) to evaluate model generalizability.

---

## 🤖 Model Performance Leaderboard

To find the most accurate price predictions, we optimized multiple algorithms using `RandomizedSearchCV`. The top-performing models achieved the following R-squared R-sqauared  scores on the test split:

1. RandomForestRegressor 🪵      🥇 95.0% Accuracy
2. XGBRegressor 🚀              🥈 94.6% Accuracy
3. GradientBoostingRegressor    🥉 94.0% Accuracy
4. LinearRegression 📈             79.0% Accuracy

---

### 💡 Key Takeaway:
The **RandomForestRegressor** model yielded the highest predictive accuracy on the test data with a score of **95.0%**, followed closely by **XGBRegressor** at **94.6%** and **GradientBoostingRegressor** at **94.0%**. Ensemble tree-based architectures significantly outperformed the baseline Linear Regression model.

---
