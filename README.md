# Insurance Premium Prediction Using Machine Learning

## 📌 Project Overview

This project focuses on predicting **health insurance premiums** using
machine learning and statistical modelling techniques.

The objective is to analyze demographic and lifestyle-related factors and
build regression models capable of predicting annual insurance charges.

The project was completed as part of the **M.Sc. Statistics** program at
**Banaras Hindu University (BHU)**.

---

## 🎯 Objectives

- Perform exploratory data analysis (EDA) to understand the dataset and
  identify important patterns.
- Preprocess the data using categorical encoding and feature scaling.
- Develop and compare multiple regression models.
- Evaluate model performance using **R², RMSE, and cross-validation**.
- Identify important factors associated with insurance premium charges.

---

## 📊 Dataset

The dataset contains **1,338 policyholders** from four major Indian cities:

- Bangalore
- Chennai
- Delhi
- Hyderabad

### Features

| Feature | Description |
|---|---|
| Age | Age of the policyholder |
| Sex | Gender of the policyholder |
| BMI | Body Mass Index |
| Children | Number of dependent children |
| Smoker | Smoking status |
| Region | City of residence |
| Charges | Annual insurance premium |

The dataset contains **no missing values**.

The target variable, `charges`, represents annual insurance premium
charges.

---

## 🔍 Exploratory Data Analysis

The analysis included:

- Distribution analysis of insurance charges
- Correlation analysis
- Correlation heatmap
- Age vs. insurance charges
- BMI vs. insurance charges
- Smoking status vs. insurance charges
- Gender vs. insurance charges
- Region vs. insurance charges
- Analysis of relationships between demographic and lifestyle variables

One of the major findings was the strong relationship between **smoking
status and insurance charges**, with a correlation of approximately
**0.79**.

Age also showed a positive relationship with charges, while BMI showed a
weaker positive relationship.

---

## 🛠️ Data Preprocessing

The following preprocessing steps were performed:

1. Converted categorical variables into numerical form using label
   encoding.
2. Applied `StandardScaler` to continuous numerical variables.
3. Divided the dataset into training and testing sets.

### Train-Test Split

- Training set: **1,070 observations (80%)**
- Test set: **268 observations (20%)**
- Random state: **42**

---

## 🤖 Machine Learning Models

Three regression models were implemented and compared:

### 1. Linear Regression

Used as the baseline regression model because of its simplicity and
interpretability.

### 2. Random Forest Regressor

An ensemble learning method used to capture nonlinear relationships and
interactions between variables.

### 3. XGBoost Regressor

A gradient boosting algorithm used to model complex nonlinear
relationships and improve predictive performance.

---

## 📈 Model Performance

| Model | Test R² | RMSE |
|---|---:|---:|
| Linear Regression | 0.7827 | 0.4798 |
| Random Forest | 0.8631 | 0.3808 |
| XGBoost | **0.8672** | **0.3750** |

XGBoost produced the highest test R² and the lowest RMSE among the three
models evaluated.

---

## 🔄 Cross-Validation

A **10-fold cross-validation** approach was used to obtain a more robust
estimate of model performance.

The Linear Regression model achieved a cross-validation score of
approximately **0.7445**.

---

## 💡 Key Insights

- **Smoking status** was the strongest predictor of insurance charges.
- Smoking status had a correlation of approximately **0.79** with
  insurance charges.
- **Age** showed a moderate positive relationship with insurance
  charges.
- **BMI** showed a weaker positive relationship with charges.
- The relationship between BMI, smoking status, and insurance charges
  showed nonlinear patterns.
- Tree-based models were able to capture nonlinear relationships better
  than Linear Regression.

---

## 🧰 Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- XGBoost
- Jupyter Notebook

---

## 📁 Project Structure

```text
insurance-premium-prediction/
│
├── data/
│   └── insurance1.csv
│
├── notebooks/
│   └── insurance_premium_prediction.ipynb
│
├── README.md
│
└── requirements.txt
