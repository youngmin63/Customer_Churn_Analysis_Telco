## 1. Background

Customer churn is a key business challenge in the telecommunications industry, as retaining existing customers is more cost-effective than acquiring new ones. Understanding why customers churn and identifying those at risk are essential for developing effective, data-driven retention strategies.

## 2. Project Objective

The objective of this project is to identify the key factors that contribute to customer churn through data analysis. Based on these insights, a machine learning model is developed to predict customers who are likely to churn.

## 3. Dataset

Source: Telco Customer Churn (IBM Sample Data Sets, Kaggle)

Key fields:

Churn – Whether a customer left the service within the last month

Tenure – Length of time the customer has stayed with the company

Contract type – Customer contract type (month-to-month, one year, two year)

Monthly charges – Amount charged to the customer on a monthly basis

Total charges – Total amount charged to the customer

Internet service & add-on services – Internet service type, online security, backup, device protection, tech support, and streaming services

Demographic information – Gender, partner status, and dependents

## 4. Exploratory Data Analysis (EDA)

Before building the predictive model, exploratory data analysis was conducted to understand customer churn patterns and identify signals related to churn behaviour.

### 4.1 Customer Churn Is Concentrated in the Early Stages of the Customer Lifecycle

<img src="/images/Tenure.png" alt="Price vs Rating" width="800" />
<p><b>Insight:</b> Churn rates are significantly higher among customers with short tenure, while long-tenure customers show much lower churn rates.
This indicates that the risk of churn is highest shortly after customer onboarding.
</p>

### 4.2 Month-to-Month Contracts Are Strongly Associated with Higher Churn

<img src="/images/ContractType.png" alt="Price vs Rating" width="800" />
<p><b>Insight:</b>Customers on month-to-month contracts exhibit substantially higher churn rates compared to those on one-year or two-year contracts.
Contract stability appears to be a key factor in retaining customers.
</p>

### 4.3 Higher Monthly Charges Increase the Likelihood of Customer Churn

<img src="/images/MonthlyCharges.png" alt="Price vs Rating" width="800" />
<p><b>Insight:</b>Customers with higher monthly charges are more likely to churn, suggesting greater price sensitivity and potential dissatisfaction among high-paying customers.
</p>

### 4.4 "Fiber Optic Internet" Users Show Higher Churn Risk

<img src="/images/Fiberoptic.png" alt="Price vs Rating" width="800" />
<p><b>Insight:</b>Churn rates are higher among customers using fiber optic internet services compared to other internet service types.
This may reflect higher service expectations or unmet performance perceptions.

</p>

### 4.5 Key EDA Insights Summary

- Churn is most prevalent during the early customer lifecycle
- Flexible contracts are associated with higher churn
- Higher prices increase churn risk
- Service type influence retention behaviour
- These insights informed feature selection and modelling decisions in the subsequent stages.

## 5. Data Preprocessing

Data preprocessing was performed to ensure data quality and prepare the dataset for machine learning modelling.

Key steps included:

- Removing non-informative identifier columns (e.g. customerID)
- Converting variables to appropriate data types and handling missing values
- Encoding categorical variables using one-hot encoding
- Scaling numerical features to ensure comparability
- Splitting the dataset into training and test sets while preserving class distribution

## 6. Churn Prediction Report
Customer churn prediction was performed to identify high-risk customers and evaluate the model’s ability to distinguish between churned and retained users.

### 6.1 Churn Prediction Model Overview

A logistic regression model was trained using customer demographics, service usage, and contract information to predict customer churn.
The model aims to identify customers at risk of churning early enough to support proactive retention strategies.

### 6.2 Classification Report and Confusion Matrix

<img src="/images/ConfusionMatrix.png" alt="Price vs Rating" width="800" />
Model performance was evaluated using accuracy, precision, recall, F1-score, and a confusion matrix.
While overall accuracy is high, recall for churned customers is prioritised due to class imbalance and the business importance of identifying at-risk user

### 6.3 ROC Curve Analysis

<img src="/images/ROC.png" alt="Price vs Rating" width="800" />
The ROC curve was used to evaluate the model’s discrimination ability across different thresholds.
The ROC-AUC score indicates good separation between churned and non-churned customers.

### 6.4 Feature Importance and Key Drivers of Churn

<img src="/images/Feature.png" alt="Price vs Rating" width="800" />
Feature importance was analysed using logistic regression coefficients.
Customer tenure and contract type were identified as the strongest predictors of churn, with short tenure and month-to-month contracts significantly increasing churn risk.

### 6.5 High-Risk Customer Profile

Based on model predictions, customers with the following characteristics are more likely to churn:

- Short tenure
- Month-to-month contracts
- High monthly charges
- Fiber optic internet service
- These customers should be prioritised for targeted retention interventions.
