# credit-risk-classification
Module 20 Supervised Machine Learning Challenge



# Credit Risk Analysis Report

## Overview of the Analysis

The purpose of this analysis is to determine  how risky a loan is based on a borrower's lending history and financial information. The data that was used includes financial information such as the size of the loan, the interest rate, the borrower's income, the amount of debt they have relative to their income, the total amount of debt they have, and how many accounts they have. The model is trying to predict whether a loan is healthy (value of 0) or at risk of default (value of 1). To make these predictions, the first step is to separate the labels set, `y` (the "loan_status" column), from the features, `X` (the rest of the columns). Then, using X and y, the data is split into training and testing datasets for the model. The training data is used to fit a Logistic Regression model, which is then used with the testing data to make predictions. The imbalanced-learn library is used to resample the data, and a second Logistic Regression model is used with the resampled data to make new predictions. Each of the two models' performance is evaluated with the balanced accuracy score, a confusion matrix, and a classification report. 

## Results

<b> Machine Learning Model 1: </b>

Description of Model 1 Accuracy, Precision, and Recall scores.
* Accuracy:
    * Accuracy is 0.99
    * Balanced accuracy score is 0.9442676901753825
    * The overall accuracy for this model is higher than the balanced accuracy score because the data is imbalanced. There are far more healthy loans in the dataset than high-risk loans, and the model correctly predicts healthy loans more often than it correctly predicts high-risk loans. For this data and model, the balanced accuracy score more accurately represents how well the model predicts both labels.

* Precision:
    * 1.00 for healthy loans
        * 100% of the predicted `0` labels were actually `0`
    * 0.87 for high-risk loans
        * 87% of the predicted `1` labels were actually `1`

* Recall:
    * 1.00 for healthy loans
        * The model correctly precited `0` 100% of the time
    * 0.89 for high-risk loans
        * The model correctly precited `1` 89% of the time



<b> Machine Learning Model 2: </b>

Description of Model 2 Accuracy, Precision, and Recall scores.
* Accuracy:
    * Accuracy is 1.00
    * Balanced accuracy score is 0.9959744975744975
    * As with the first model, the imbalanced data results in a higher overall accuracy score than balanced accuracy score, but the difference in the two scores is much smaller than the first model. This model is more accurate in predicting both labels than the first model. 

* Precision:
    * 1.00 for healthy loans
        * 100% of the predicted `0` labels were actually `0`
    * 0.87 for high-risk loans
        * 87% of the predicted `1` labels were actually `1`

* Recall:
    * 1.00 for healthy loans
        * The model correctly precited `0` 100% of the time
    * 1.00 for high-risk loans
        * The model correctly precited `1` 100% of the time

## Summary

The second machine learning model makes more accurate predictions for both labels than the first model does. It is likely more important to be able to correctly predict `1`s than `0`s because it would be more costly to label a high-risk loan as healthy than it would be to label a healthy loan as risky. However, we want the model to be able to accurately predict both labels in order to maximize profits. The precision for each model is the same, but the accuracy, balanced accuracy, and recall are all higher for the second machine learning model than the first. The second machine learning model performs best and would be the better model to use.
