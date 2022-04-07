# **Prediction of Loan Approval Using Machine Learning**

* Oleksandra Aliyeva
* April 2022

**Goal:**

The goal of this project is to predict approval or disapproval of Loan Application.

**Source of DATA**: [Kaggle](https://www.kaggle.com/datasets/vikramkumar001/partial-bank-loan-dataset)


The dataset consists of 5584 rows, and 13 columns.The columns represent 12 features and 1 target variable.

| Feature            | Description        
| :------------------|:-----------------------------------------------| 
| Loan_ID            |Unique loan ID                                  | 
| Gender             |Male/Female                                     |  
| Married            |Marriage status (TRUE/FALSE)                    | 
| Dependent_No       |Number of dependent/s                           | 
| Education          |Education status (Graduate/Not Graduate)        |  
| Self_Employed      |Employment status (TRUE/FALSE)                  | 
| Applicant_Income   |Amount of applicant's income                    | 
| CoApplicant_Income |Amount of coapplicant's income                  |  
| Loan_Amount        |Amount of loan requested                        | 
| LoanAmountTerm     |Term of loan in months                          | 
| Credit_History     |Applicant's credit history (0 for no /1 for yes)|  
| Property_District  |Applicant's district of property owned          | 
| Loan_Status        |Loan approval status (0 for no /1 for yes)      | 

**Model Comparison Summary**

| Model                         | Accuracy   |Precision Class 0|Precision Class 1 |Recall  Class 0|Recall  Class 1 |F1 Class 0 |F1 Class 1    |
|:------------------------------|:-----------|:----------------|:-----------------|:--------------|:---------------|:----------|:-------------|
|KNN                            |0.65        |0.33             |0.67              |0.06           |0.94            |0.1        |0.78          | 
|Random Forest                  |0.58        |0.34             |0.67              |0.28           |0.73            |0.31       |0.7           | 
|LGBM Classifier                |0.63        |0.3              |0.66              |0.09           |0.9             |0.14       |0.76          |
|SMOTE with Logistic Regression |0.49        |0.32             |0.66              |0.49           |0.49            |0.39       |0.56          | 
|SMOTE with Random Forest       |0.61        |0.33             |0.67              |0.18           |0.82            |0.23       |0.74          |

* Comparison Summary of Models used in this project: KNN, Random Forest, LGBM Classifier, SMOTE with Logical Regression and SMOTE with Random Forest. If we compare acuraccy for testing set we can see that best results has KNN Model (65%), but if we take in consideration how well our classes are predicted we should choose a Random Forest. We don't want to approve a loan to a person that has chances of not paying it off, that is why we have to find the model thad has less mistakes in predictions of class 0 (less false positives). Random Forest has accuracy of 58%, model predicts class 0 better than other models, 28% of class 0 and 73% of class 1 are predicted correctly.

**Recommendations**

* Re-consider the application process in order to eliminate the luck of critical data required for adjudication by making certain fields as mandatory
* Extend the application to include additional information about:
  * purpose of the loan
  * debt-to-income ratio


[Technical Presentation](https://github.com/AliyevaO/Loan/blob/main/Technical%20Presentation%20Loan%20Prediction)
