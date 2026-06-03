# car-price-prediction

```markdown
# 🚗 Car Price Prediction 

Welcome to the Audi Car Price Prediction project repository! This project focuses on building an end-to-end Machine Learning pipeline to predict the prices of used Audi cars based on features like model, year, mileage, fuel type, engine size, and transmission.

A heavy emphasis is placed on comprehensive Exploratory Data Analysis (EDA) using NumPy, Pandas, Matplotlib, and Seaborn, followed by rigorous data preprocessing and regression model evaluation.

---

## 📊 Dataset Overview

The analysis is performed on the `audi.csv` dataset, which contains historical listings of Audi cars.

* Dataset Dimensions:  The dataset contains **10,668 records** and **9 distinct features** including the target variable `price'.
* Target Variable: `price` (Numerical)

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
A deep-dive analysis was performed by comparing the target variable `price` against all independent variables to capture underlying trends and patterns:
* Visualized structural distributions and price ranges across different car models and years.
* Analyzed the negative correlation between `mileage` and `price`.
* Plotted categorical impacts such as `transmission` type and `fuelType` on overall price distribution.

### 2. Data Preprocessing & Feature Engineering
* **Categorical Encoding:** Leveraged `LabelEncoder` from Scikit-Learn to convert non-numeric categorical variables like `model`, `transmission`, `fuelType` into structured numerical representations.
* **Feature Scaling:** Applied `StandardScaler` from Scikit-Learn to standardize the features in the dataset, ensuring a uniform scale across features before training.
* **Data Splitting:** Divided the dataset into training and testing sets with an **80/20 split** (`test_size=0.2`) to evaluate model generalizability.

---

## 🤖 Models Trained & Performance Evaluation

Multiple regression models were trained, tuned, and evaluated on the test dataset. Hyperparameter optimization was conducted via **RandomizedSearchCV** to identify optimal estimator parameters.

| Machine Learning Model | Key Highlights / Approach | Performance (R² Accuracy) |
| :--- | :--- | :---: |
| **XGBRegressor** | Gradient Boosting trees via Extreme Gradient Boosting | **94.6%** (0.946) 🏆 |
| **GradientBoostingRegressor** | Sequential ensemble learning method | **94.0%** (0.94) |
| **RandomForestRegressor** | Bagging ensemble with multiple decision trees | Trained & Evaluated |
| **LinearRegression** | Baseline parametric regression approach | Trained & Evaluated |

---
### Key Takeaway:
The **XGBRegressor** model yielded the highest predictive accuracy on the test data with a score of **94.6%**, followed closely by the **GradientBoostingRegressor** at **94.0%**.

---
