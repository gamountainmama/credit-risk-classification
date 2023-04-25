# Module 20 Report 

## Overview of the Analysis

I completed an analysis using supervised machine learning methods for loan approvals based on: 
- the size of the loan
- the interest rate
- the borrower's income
- the borrower's debt-to-income ratio
- the number of accounts
- the number of derogatory marks
- total debt

I predicted whether a loan was healthy or high-risk. The original data included 75,036 healthy loans and 2,500 high-risk loans.

1. I split the original data into training and testing datasets using train_rest_split in sklearn.model_selection.
2. I fit the model using LogisticRegression, also from sklearn.model_selection.
3. I created a dataframe to compare the predictions and the actual results.
4. I evaluated the model using accuracy_score, a confusion matrix, and classification_report from sklearn.metrics.
5. I then re-sampled the data using RandomOverSampler from imblearn.over_sampling to artificial create the same number of healthy and high-risk loans.
6. I re-ran my analysis using the re-sampled data.


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Model 1 (original data) had an accuracy score of 0.9924, precision of 1.00 for the healthy loans and 0.88 for the high-risk loans. The recall scores were 1.00 for healthy loans and 0.91 for high-risk loan. This model is most likely to predict accurately for healthy loans.

* Machine Learning Model 2:
  * Model 2 (re-sampled data) had an accuracy score of 0.9950, precision of 1.00 for the healthy loans and 0.99 for the high-risk loans. The recall scores were 0.99 for healthy loans and 1.00 for high-risk loan. This model predicts accurately for both types of loans.


## Summary

The re-sampled data model seems to perform best because it is more accurate and more precise that the original data model. It is more important to accurately predict the high-risk loans so that banks are more cautious with these loans.
