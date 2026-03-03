# Telco Customer Churn Prediction

An end-to-end **Machine Learning project** that predicts whether a telecom customer is likely to **churn (leave the service)**.  
The project follows **industry best practices** including data preprocessing pipelines, feature engineering, multiple ML models, and performance optimization.

---

## Project Overview

Customer churn is a major challenge in the telecom industry.  
This project uses historical customer data to build a **binary classification model** that identifies customers who are likely to churn, enabling proactive retention strategies.

---

## Problem Statement

To predict whether a customer will **churn (Yes/No)** based on:
- Demographic details  
- Account information  
- Service usage  
- Billing and payment behavior  

This is a **supervised binary classification problem**.

---

## Dataset

- **Name:** Telco Customer Churn Dataset  
- **Source:** Kaggle  
- **Target Variable:** `Churn`  
  - `Yes` → 1  
  - `No` → 0  

Each row represents a customer, and columns include numerical and categorical features.

---

## Features Used

### Numerical Features
- tenure  
- MonthlyCharges  
- TotalCharges  
- AvgCharges *(engineered)*  

### Categorical Features
- gender  
- SeniorCitizen  
- Partner  
- Dependents  
- PhoneService  
- MultipleLines  
- InternetService  
- OnlineSecurity  
- OnlineBackup  
- DeviceProtection  
- TechSupport  
- StreamingTV  
- StreamingMovies  
- Contract  
- PaperlessBilling  
- PaymentMethod  

---

## Tech Stack

- **Language:** Python  
- **Libraries:**  
  - pandas, numpy  
  - scikit-learn  
  - matplotlib (optional)  
- **Environment:** Google Colab / Jupyter Notebook  

---

## Project Workflow

Data Loading
↓
Data Cleaning
↓
Feature Engineering
↓
Preprocessing Pipeline
↓
Train-Test Split
↓
Model Training
↓
Model Evaluation
↓
Performance Improvement

---

## Data Preprocessing

- Converted `TotalCharges` from string to numeric
- Handled missing values using **SimpleImputer**
- Scaled numerical features using **StandardScaler**
- Encoded categorical features using **OneHotEncoder**
- Used **Pipeline** and **ColumnTransformer** to prevent data leakage

---

## Models Implemented

Each model is given a **unique identifier**:

| Model Name | Algorithm |
|----------|----------|
| LR-ChurnNet | Logistic Regression |
| KNN-ChurnScope | K-Nearest Neighbors |
| DT-ChurnTree | Decision Tree |
| RF-ChurnForest | Random Forest |
| GB-ChurnBoost | Gradient Boosting |

---

## Evaluation Metrics

Due to class imbalance, accuracy alone is not sufficient.  
The following metrics are used:

- **Accuracy**
- **Precision**
- **Recall**
- **F1-Score** 
- **ROC-AUC** 

> F1-Score and ROC-AUC are prioritized for churn prediction.

---

## 🚀 Model Performance Improvement Techniques

The following techniques were applied to improve model performance:

###  Feature Engineering
- Average monthly charges per tenure
- High monthly charge indicator

###  Class Imbalance Handling
- Used `class_weight='balanced'`

###  Stronger Models
- Ensemble models like **Random Forest** and **Gradient Boosting**

###  Hyperparameter Tuning
- Used `GridSearchCV` for optimal parameters

###  Threshold Tuning
- Adjusted probability threshold to improve Recall and F1-Score

---

##  Best Model

- **Random Forest (RF-ChurnForest)**  
- Achieved the best balance between **Recall**, **F1-Score**, and **ROC-AUC**

---

##  Results Summary

- Ensemble models outperformed linear models
- Feature engineering had a significant impact on performance
- Threshold tuning improved churn detection effectiveness

---

##  How to Run the Project

1. Clone the repository
```bash
git clone https://github.com/your-username/telco-churn-prediction.git
2. Open the notebook in Google Colab or Jupyter Notebook

3. Upload the dataset (Telco-Customer-Churn.csv)

4. Run cells step by step
