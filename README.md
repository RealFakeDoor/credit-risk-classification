# Credit Risk Classification

## Credit Risk Analysis Report

### Purpose of the Analysis
The purpose of this analysis is to develop a logistic regression model to predict the likelihood of a loan being high-risk based on given features. This model can assist financial institutions in making informed lending decisions, thereby mitigating credit risk.

### Financial Information and Predictions
Each loan was classified using the following information for that loan:

- **Loan Size**: The total amount of money borrowed by the applicant.
- **Interest Rate**: The percentage of the loan amount charged by the lender as interest to the borrower, typically expressed annually.
- **Borrower Income**: The total annual income of the loan applicant.
- **Debt to Income Ratio**: The ratio of the borrower’s monthly debt payments to their monthly gross income, used to assess their ability to manage monthly payments and repay debts.
- **Number of Accounts**: The total number of credit accounts (such as credit cards, loans, etc.) the borrower currently holds.
- **Derogatory Marks**: Negative records on the borrower's credit report, such as bankruptcies or late payments, which can affect creditworthiness.
- **Total Debt**: The total amount of outstanding debt that the borrower currently owes.
- **Loan Status**: The current status of the loan, where 0 indicates a healthy loan and 1 indicates a high-risk loan that may default.

### Variable Prediction Counts
From the 'y' variable, the following value counts indicate the current distribution of healthy loans vs high-risk loans:
- There are 75,000 healthy loans (0) and 2,500 high-risk loans (1) in the dataset.

### Prediction Results Data
- **True Positives (TP)**: 563 (High-risk loans correctly predicted as high-risk)
- **False Negatives (FN)**: 56 (High-risk loans incorrectly predicted as healthy)
- **False Positives (FP)**: 102 (Healthy loans incorrectly predicted as high-risk)
- **True Negatives (TN)**: 18,663 (Healthy loans correctly predicted as healthy)

### Stages of the Machine Learning Process
**Machine Learning Steps**
1. **Data Collection & Data Preparation**: Lending data was imported into a dataframe for analysis, separated into the target variable (loan_status) and feature variables (all other variables) into y and X, respectively. The data was then split into training and testing datasets.
2. **Model Selection**: Logistic Regression was chosen as the model for this analysis due to its effectiveness in binary classification problems.
3. **Model Training**: The logistic regression model was instantiated with a random state to ensure reproducibility and trained on X_train and Y_train datasets.
4. **Model Prediction**: Predictions were made using the trained model on the testing dataset (X_test).
5. **Model Evaluation**: The evaluation metrics were interpreted to understand the model’s effectiveness in predicting both healthy and high-risk loans.

### Methods Used
**Logistic Regression**: Designed for binary classification tasks, making it a natural choice for problems where the outcome is dichotomous, such as predicting loan status (healthy vs. high-risk). Logistic Regression provides probability estimates and is computationally efficient.

## Results

**Machine Learning Model: Logistic Regression**

- **Accuracy**: 0.99
- **Precision**:
  - Healthy loans (0): 1.00
  - High-risk loans (1): 0.85
- **Recall**:
  - Healthy loans (0): 0.99
  - High-risk loans (1): 0.91

## Summary

The model's accuracy is 99%, meaning that 99% of the time, the model's predictions (both for healthy and high-risk loans) are correct. This high accuracy is a strong indicator of the model's reliability.

### Precision Insights
- **Healthy Loans (0)**: The precision is 1.00, indicating that all loans predicted as healthy are indeed healthy. This perfect precision is crucial for minimizing false positives, ensuring that borrowers who are predicted as low-risk truly are low-risk.
- **High-Risk Loans (1)**: The precision is 0.85, meaning that 85% of the loans predicted as high-risk are actually high-risk. While this is not as high as the precision for healthy loans, it still shows good performance in identifying risky loans.

### Recall Insights
- **Healthy Loans (0)**: The recall is 0.99, indicating that 99% of the actual healthy loans are correctly identified by the model. This high recall ensures that most healthy loans are not incorrectly classified as high-risk, reducing the likelihood of unnecessarily rejecting good applicants.
- **High-Risk Loans (1)**: The recall is 0.91, meaning that 91% of the actual high-risk loans are correctly identified. This high recall is important for minimizing the number of risky loans that are incorrectly classified as healthy, thus protecting the lender from potential defaults.

### F1-Score
The F1-score balances precision and recall, providing a single metric that considers both false positives and false negatives.
- **Healthy Loans (0)**: The F1-score is 1.00, indicating excellent performance.
- **High-Risk Loans (1)**: The F1-score is 0.88, showing good but not perfect performance. This suggests there is some room for improvement in predicting high-risk loans.

### Importance of Class Distribution
The dataset is highly imbalanced, with many more healthy loans (18,765) compared to high-risk loans (619). Despite this imbalance, the model performs well in both precision and recall for high-risk loans, which is often challenging in imbalanced datasets.

### Model Recommendations
- **Reliability**: Given the high accuracy, precision, and recall, the model is highly reliable and can be confidently used by financial institutions to assess loan risk.
- **Risk Management**: The model’s ability to accurately identify high-risk loans (with a recall of 0.91) makes it a valuable tool for managing and mitigating credit risk.
- **Customer Satisfaction**: The high precision and recall for healthy loans ensure that most good loan applicants are approved, maintaining customer satisfaction and trust.

The logistic regression model demonstrates excellent performance in predicting loan status, achieving high accuracy, precision, and recall for both healthy and high-risk loans. Its reliability in identifying risky loans and accurately approving healthy loans makes it a valuable tool for financial institutions. While there is a slight room for improvement in predicting high-risk loans, the current model's performance is strong enough to recommend its use for credit risk assessment.
