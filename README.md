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
