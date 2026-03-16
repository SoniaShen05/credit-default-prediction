# credit-default-prediction
Machine learning project for predicting credit card default risk using customer financial behavior data. Includes data preprocessing, feature engineering, class imbalance handling, and model comparison (Logistic Regression and XGBoost). Provides insights into key drivers of credit risk such as repayment history and billing patterns.

## Dataset
The dataset contains 30,000 credit card clients and includes demographic information, credit limits, bill statements, and payment history.

Key variables include:

- Credit limit (LIMIT_BAL)
- Payment status history (PAY_0 – PAY_6)
- Bill amounts (BILL_AMT1 – BILL_AMT6)
- Payment amounts (PAY_AMT1 – PAY_AMT6)
- Target variable: default_payment_next_month

## Data Processing

Key preprocessing steps include:

- Handling categorical variables (education, marriage)
- One-hot encoding for Logistic Regression
- Standardization of numerical features
- Addressing class imbalance using **SMOTE**

## Models Implemented

Two models were trained and compared:

- Logistic Regression
- XGBoost

Evaluation metrics include:

- Recall
- F1 Score
- ROC-AUC

## Results

| Model | Recall | F1 Score | ROC-AUC |
|------|------|------|------|
| Logistic Regression | 0.63 | 0.46 | 0.66 |
| XGBoost | 0.47 | 0.48 | 0.66 |

The Logistic Regression model achieved higher recall for detecting default customers, which can be valuable in risk management contexts.

## Feature Importance

Key predictors of default include:

- Recent repayment status (PAY_0)
- Recent bill amount (BILL_AMT1)
- Credit limit (LIMIT_BAL)
- Payment amounts

## Key Insight

Recent repayment behavior is the strongest predictor of default risk.

This analysis demonstrates how machine learning models can help financial institutions identify high-risk customers and improve credit risk management.

## Tools

Python  
Pandas  
Scikit-learn  
XGBoost  
Seaborn  
Matplotlib
