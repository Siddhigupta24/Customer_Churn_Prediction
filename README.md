# Customer Churn Prediction using Machine Learning

## Project Overview
Customer churn is a major challenge for subscription-based businesses. This project focuses on predicting whether a telecom customer is likely to churn based on customer demographics, service usage, and billing information.

The project compares:
- Baseline Machine Learning Model
- Feature Engineered Model
- Feature Selected Model

to evaluate how feature engineering impacts churn prediction performance.

---

## Problem Statement
Customer churn occurs when customers stop using a company's service. Predicting churn helps businesses improve retention strategies and reduce revenue loss.

Goal:
Build a machine learning model to accurately predict customer churn.

---

## Dataset
Dataset: Telco Customer Churn Dataset  
Total Records: 7043  
Features: 21  

Key features include:
- Gender
- Tenure
- Contract Type
- Monthly Charges
- Total Charges
- Internet Services
- Payment Method

Target Variable:
- Churn (Yes / No)

---

## Tech Stack
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab

---

## Data Preprocessing
- Converted `TotalCharges` to numeric
- Handled missing values using median imputation
- Encoded target variable (Yes/No → 1/0)
- Standardized numerical features
- Applied One-Hot Encoding for categorical variables

---

## Feature Engineering
New features created:
- **Tenure Group** → Binned customer tenure into categories
- **Number of Additional Services** → Count of subscribed services
- **Monthly Charge Ratio** → Monthly charges divided by tenure

These engineered features improved model performance.

---

## Models Used
- Logistic Regression
- Random Forest Classifier

---

## Model Performance

| Model | Accuracy | F1 Score (Churn) |
|-------|----------|------------------|
| Baseline Model | 0.80 | 0.60 |
| Feature Engineered Model | 0.81 | 0.59 |
| Selected Features Model | 0.81 | 0.59 |

---

## Key Insights
- Feature engineering improved overall accuracy from **80% to 81%**
- Contract type and billing-related features were highly influential
- Random Forest helped identify the most important features

---

## Future Improvements
- Hyperparameter tuning
- Try XGBoost / LightGBM
- Improve churn recall score
- Deploy model using FastAPI or Streamlit
