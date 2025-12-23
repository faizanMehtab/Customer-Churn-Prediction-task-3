📉 Task 3: Customer Churn Prediction
📌 Objective

The goal of this task is to predict customer churn—whether a customer is likely to leave a telecom service—using historical customer data. This helps businesses design customer retention strategies and reduce revenue loss.

📊 Dataset Description

The dataset contains 7,043 customer records with 21 features, including:

Customer Information: Gender, SeniorCitizen, Partner, Dependents

Service Usage: PhoneService, InternetService, Streaming services, TechSupport

Billing Details: MonthlyCharges, TotalCharges, Contract, PaymentMethod

Target Variable:

Churn → Yes (Customer left), No (Customer stayed)

## Data Cleaning & Preprocessing

Removed customerID since it does not affect prediction.

Converted TotalCharges from object to numeric type.

Missing values in TotalCharges were filled using the median.

Target variable Churn was encoded as:

Yes → 1

No → 0

Categorical features were converted using One-Hot Encoding.

Data split into 80% training and 20% testing sets.

## Exploratory Analysis

Feature importance was extracted from the trained Random Forest model to understand which factors influence churn the most.

## Model Used

Random Forest Classifier

Number of trees: 100

Random State: 42

📊 Model Evaluation
🔹 Accuracy

78.9%

🔹 Confusion Matrix
[[941  95]
 [202 171]]

🔹 Interpretation

True Negatives (941): Customers who stayed and were correctly predicted.

False Positives (95): Customers predicted to churn but actually stayed.

False Negatives (202): Customers who churned but were predicted to stay (critical risk).

True Positives (171): Customers who churned and were correctly identified.

The model performs well overall but slightly underestimates churners, indicating scope for further improvement.

## Feature Importance Insights

Top factors influencing customer churn include:

Contract Type: Month-to-month contracts show higher churn risk.

Tenure: Long-term customers are less likely to churn.

Monthly Charges: Higher charges increase churn probability.

Internet & Online Services: Usage patterns affect retention.



##      Business Implications

Focus retention efforts on:

Customers with month-to-month contracts

Customers with high monthly charges

New customers with low tenure

Personalized offers, discounts, and improved service quality can significantly reduce churn.

🛠 Tools & Technologies

Python

Pandas, NumPy

Scikit-learn

Matplotlib

Jupyter Notebook