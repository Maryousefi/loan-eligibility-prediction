# Loan Eligibility Prediction

This project automates the process of determining whether an individual is eligible for a loan using advanced machine learning techniques. The dataset includes various demographic and financial attributes of loan applicants.

## Objective

To automate the loan approval eligibility process based on historical data using and comparing multiple machine learning models.

## Dataset Features

- **Gender**: Male / Female  
- **Married**: Yes / No  
- **Dependents**: 0 / 1 / 2 / 3+  
- **Education**: Graduate / Not Graduate  
- **Self_Employed**: Yes / No  
- **ApplicantIncome**: Numeric  
- **CoapplicantIncome**: Numeric  
- **LoanAmount**: Numeric  
- **Loan_Amount_Term**: Loan term in days  
- **Credit_History**: 1 (Good) / 0 (Bad)  
- **Property_Area**: Urban / Semiurban / Rural  
- **Loan_Status**: Y (Approved) / N (Rejected)

## Project Workflow

### 1. Data Preprocessing

- Handling missing values using mean/mode strategies
- Label encoding of categorical variables
- Normalization of numerical features using StandardScaler
- Feature engineering: added `Total_Income` and `Loan_to_Income_Ratio`
- Class balancing using SMOTE
- Data split:
  - Training (65%)
  - Validation (20%)
  - Test (15%)

### 2. Modeling

- Logistic Regression
- K-Nearest Neighbors (KNN) with hyperparameter tuning using GridSearchCV
- Artificial Neural Network (ANN) with:
  - GridSearchCV for tuning layers, activation functions, and solvers
  - Early stopping to prevent overfitting
  - Increased `max_iter` to improve convergence

### 3. Model Evaluation

- Evaluation metrics:
  - Accuracy
  - Precision, Recall, F1-Score
- Confusion Matrix visualization
- Comparison of all models on validation and test sets

### 4. Optimization & Improvements

- Feature Engineering:
  - `Total_Income` = `ApplicantIncome` + `CoapplicantIncome`
  - `Loan_to_Income_Ratio` = `LoanAmount` / `Total_Income`
- Hyperparameter tuning using GridSearchCV for both KNN and ANN
- Addressed class imbalance using SMOTE
- Used early stopping and increased iteration count to avoid convergence issues with ANN

## Visualizations

Visual analysis using Seaborn and Matplotlib includes:

- Count plots for `Loan_Status`
- Effect of `Credit_History` on approvals
- Distribution of applicant and co-applicant incomes
- Confusion matrix for each model

## Getting Started

### Installation

Clone the repository:

```bash
git clone https://github.com/maryousefi/loan-eligibility-prediction.git
cd loan-eligibility-prediction
