# credit-risk-classification

**Credit Risk Analysis Report** 

* Explain the purpose of the analysis.
The purpose of this analysis is to develop a logistic regression model to predict the likelihood of a loan being high-risk based on given features. This model can assist financial institutions in making informed lending decisions, thereby mitigating credit risk.

* Explain what financial information the data was on, and what you needed to predict.

Each loan was classified using the following information for that loan;

    **Loan Size**: The total amount of money borrowed by the applicant.

    **Interest Rate**: The percentage of the loan amount charged by the lender as interest to the borrower, typically expressed annually.

    **Borrower Income**: The total annual income of the loan applicant.

    **Debt to Income Ratio**: The ratio of the borrower’s monthly debt payments to their monthly gross income, used to assess their ability to manage monthly payments and repay debts.

    **Number of Accounts**: The total number of credit accounts (such as credit cards, loans, etc.) the borrower currently holds.

    **Derogatory Marks**: Negative records on the borrower's credit report, such as bankruptcies or late payments, which can affect creditworthiness.

    **Total Debt**: The total amount of outstanding debt that the borrower currently owes.

    **Loan Status**: The current status of the loan, where 0 indicates a healthy loan and 1 indicates a high-risk loan that may default.
   
   

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
From the 'y' variable the following value counts indicate the current distribution of healthy loans vs high-risk-loans.
There are 75,000 healthy loans (0) and 2,500 high-risk loans (1) in the dataset.

    
* Describe the stages of the machine learning process you went through as part of this analysis.   
 **Machine Learning Steps** 
     Data Collection & Data Preparation - Lending data was imported into a dataframe for analysis, this data was then seperated into the target variable (loan_status) and feature variables (all other variables) were separated into y and X, respectively. the data was then split into training and testing data sets.
     
     Model Selection - Logistic Regression was chosen as the model for this analysis due to its effectiveness in binary classification problems.
     
     Model Training - The logistic regression model was instantiated with a random state to ensure reproducibility and trained in X_train and Y_train datasets.
     
     Model Prediction - Predictions were made using the trained model on the testing dataset (X_test).
     
     Model Evaluation - The evaluation metrics were interpreted to understand the model’s effectiveness in predicting both healthy and high-risk loans.
 
 

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithm).
Logistic Regression is designed for binary classification tasks, making it a natural choice for problems where the outcome is dichotomous, such as predicting loan status (healthy vs. high-risk). Futhermore Logistic Regression provides probability estimates and are computationally efficient.


## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    * Description of Model 1 Accuracy, Precision, and Recall scores.
    
 *The results*:

    **Accuracy**: 0.99

    **Precision**:
        Healthy loans (0): 1.00
        High-risk loans (1): 0.85

    **Recall**:
        Healthy loans (0): 0.99
        High-risk loans (1): 0.91

## Summary

Summarise the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.
