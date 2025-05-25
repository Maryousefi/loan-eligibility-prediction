# Loan Eligibility Prediction

This project automates the process of determining whether an individual is eligible for a loan using machine learning techniques. The dataset includes various demographic and financial attributes of loan applicants.

## Objective

To automate the loan approval eligibility process based on historical data using machine learning models.

## Dataset Features

* **Gender**: Male / Female
* **Married**: Yes / No
* **Dependents**: 0 / 1 / 2 / 3+
* **Education**: Graduate / Not Graduate
* **Self\_Employed**: Yes / No
* **ApplicantIncome**: Numeric
* **CoapplicantIncome**: Numeric
* **LoanAmount**: Numeric
* **Loan\_Amount\_Term**: Loan term in days
* **Credit\_History**: 1 (Good) / 0 (Bad)
* **Property\_Area**: Urban / Semiurban / Rural
* **Loan\_Status**: Y (Approved) / N (Rejected)

## Project Workflow

### 1. Data Preprocessing

* Handle missing values
* Encode categorical variables
* Normalize numeric features
* Split data into training (65%), validation (20%), and test sets (15%)

### 2. Modeling

* Logistic Regression
* K-Nearest Neighbors (KNN)
* Artificial Neural Network (ANN)

### 3. Model Evaluation

* Accuracy
* Precision, Recall, F1-Score
* Comparison across models

### 4. Optimization Techniques

* Feature Engineering (e.g., `Total_Income`)
* Class balancing using SMOTE
* Visual insights using Seaborn

## Visualizations

Visual analysis using Seaborn includes:

* Count plots of Loan Status
* Effect of Credit History
* Income distribution analysis


## Getting Started

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/maryousefi/loan-eligibility-prediction.git
   cd loan-eligibility-prediction
   ```

2. Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Run the Jupyter Notebook:

   ```bash
   jupyter notebook "Maryam'sproject_final.ipynb"
   ```
