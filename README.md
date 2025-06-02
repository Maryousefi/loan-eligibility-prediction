# <span style="color:#1E90FF;">Loan Eligibility Prediction</span>

This project automates the process of determining whether an individual is eligible for a loan using advanced machine learning techniques. The dataset includes various demographic and financial attributes of loan applicants.

## <span style="color:#1E90FF;">Objective</span>

To automate the loan approval eligibility process based on historical data using and comparing multiple machine learning models.

## <span style="color:#1E90FF;">Dataset Features</span>

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

## <span style="color:#1E90FF;">Project Workflow</span>

### <span style="color:#1E90FF;">1. Data Preprocessing</span>

- Handling missing values using mean/mode strategies  
- Label encoding of categorical variables  
- Normalization of numerical features using StandardScaler  
- Feature engineering: added `Total_Income` and `Loan_to_Income_Ratio`  
- Class balancing using SMOTE  
- Data split:  
  - Training (65%)  
  - Validation (20%)  
  - Test (15%)

### <span style="color:#1E90FF;">2. Modeling</span>

- Logistic Regression  
- K-Nearest Neighbors (KNN) with hyperparameter tuning using GridSearchCV  
- Artificial Neural Network (ANN) with:  
  - GridSearchCV for tuning layers, activation functions, and solvers  
  - Early stopping to prevent overfitting  
  - Increased `max_iter` to improve convergence

### <span style="color:#1E90FF;">3. Model Evaluation</span>

- Evaluation metrics:  
  - Accuracy  
  - Precision, Recall, F1-Score  
- Confusion Matrix visualization  
- Comparison of all models on validation and test sets

### <span style="color:#1E90FF;">4. Optimization & Improvements</span>

- Feature Engineering:  
  - `Total_Income` = `ApplicantIncome` + `CoapplicantIncome`  
  - `Loan_to_Income_Ratio` = `LoanAmount` / `Total_Income`  
- Hyperparameter tuning using GridSearchCV for both KNN and ANN  
- Addressed class imbalance using SMOTE  
- Used early stopping and increased iteration count to avoid convergence issues with ANN

## <span style="color:#1E90FF;">Visualizations</span>

Visual analysis using Seaborn and Matplotlib includes:

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
```

Create and activate a virtual environment (optional but recommended):

```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows
```

Install required packages:

```bash
pip install -r requirements.txt
```

### Usage

Run the main script or notebook to train and evaluate the models.

## License

MIT License

## Contact

For questions or contributions, please open an issue or submit a pull request.
