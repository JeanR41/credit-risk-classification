# Credit Risk Classitication

## Overview
This project aims to build a supervised learning model to predict loan default risk based on a variety of borrower features. The dataset used for training the model contains information on loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, total debt, and the loan status (whether the loan is considered defaulted or not). A logistic regression model is used for classification, and the model's performance is evaluated using a confusion matricx and a classification report of precision, recall, and F1-score.

## Requirements

The following libraries should be installed prior to running the model.

 * import numpy as np
 * import pandas as pd
 * from pathlib import Path
 * from sklearn.metrics import confusion_matrix, classification_report
 * from sklearn.model_selection import train_test_split
 * from sklearn.linear_model import LogisticRegression

## Usage
To use this model, you can follow these steps:
1. Load your dataset into a Pandas DataFrame.
2. Separate the target variable (loan_status) and the feature variables.
3. Split the data into training and testing sets.
4. Train a logistic regression model using the training data.
5. Make predictions on the testing data.
6. Evaluate the model's performance using the confusion matrix and classification report.

## Conclusion
**Question:** How well does the logistic regression model predict both the `0` (healthy loan) and `1` (high-risk loan) labels?

**Answer:** 
The confusion matrix shows that the model predicted 18,655 healthy loans (0) correctly, with only 110 misclassifications (false positives). For high-risk loans (1), it correctly predicted 583 instances, with only 36 misclassifications (false negatives). This indicates that the model performs very well on both classes, especially on the healthy loans.

Overall, the logistic regression model performs exceptionally well in predicting both the 0 (healthy loan) and 1 (high-risk loan) labels. The model achieved an overall accuracy of 99%, with perfect precision for healthy loans (0) and a high recall of 94% for high-risk loans (1). This suggests that while the model is highly effective at identifying healthy loans, it also maintains a strong ability to correctly identify high-risk loans, making it a reliable tool for assessing loan applications.