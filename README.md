# loan-eligibility-prediction
# Loan Eligibility Prediction

This project aims to automate the process of determining whether an individual is eligible for a loan using machine learning techniques. The dataset contains various demographic and financial attributes of loan applicants.

## Objective
Automate the loan approval eligibility process based on historical data.

## Dataset Features

- Gender: Male / Female
- Married: Yes / No
- Dependents: 0 / 1 / 2 / 3+
- Education: Graduate / Not Graduate
- Self_Employed: Yes / No
- ApplicantIncome: Numeric
- CoapplicantIncome: Numeric
- LoanAmount: Numeric
- Loan_Amount_Term: Loan term in days
- Credit_History: 1 (good), 0 (bad)
- Property_Area: Urban / Semiurban / Rural
- Loan_Status: Y (approved) / N (rejected)

## Project Steps

### 1. Preprocessing
- Handling missing values
- Label encoding categorical features
- Normalization of numeric features
- Splitting data (65% train / 20% validation / 15% test)

### 2. Modeling
- Logistic Regression
- K-Nearest Neighbors
- Artificial Neural Network

### 3. Evaluation
- Accuracy
- Precision, Recall, F1-Score
- Comparison across models

### 4. Optimization
- Feature Engineering (Total_Income)
- SMOTE for class balancing
- Visual insights with Seaborn

## Visualizations
Included with Seaborn:
- Countplots of Loan Status
- Credit History effect
- Income distribution analysis

## Requirements

```bash
pip install -r requirements.txt

## Run Locally

Clone the project and run the notebook:

```bash
git clone https://github.com/yourusername/loan-eligibility-prediction.git
cd loan-eligibility-prediction
jupyter notebook "Maryam'sproject_Final.ipynb"
