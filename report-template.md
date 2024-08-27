# Module 12 Credit Risk Classification Report

## Overview of the Analysis

The purpose of this analysis was to develop a classification model to predict and categorize credit risk. The goal was to use machine learning algorithms to assess the creditworthiness of loan applicants and classify them into either healthy loans or high-risk loans based on various financial attributes. The data used in the analysis included information on 77536 loans, and included the loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, total debt, and loan status for each applicant. The model will predict the loan status for the applicant, which has been classified as either healthy or high-risk.

The stages of the machine learning process for this analysis were as follows:
1. Data Preparation: Importing the dataset, exploring the features, and preparing the data for modeling.
2. Data Splitting: Separating the data into features and labels, and splitting it into training and testing sets.
3. Model Selection: Choosing a suitable classification algorithm for the task, in this case logistic regression.
4. Model Training: Fitting the selected model on the training data.
5. Model Evaluation: Assessing the model's performance using metrics like accuracy, precision, recall, and F1 score.
 
The primary model utilized in this analysis was logistic regression from the scikit-learn library. Additionally, supporting functions like train_test_split for data splitting, and evaluation functions like confusion_matrix and classification_report were used to assess the model's performance. The analysis also involved comparing multiple classification algorithms to determine the most effective model for predicting credit risk.

## Results

* Machine Learning Model (Logistical Regression):
    * Accuracy:
        * General Description - Accuracy represents the overall correctness of the model's predictions. It is calculated as the ratio of correctly predicted instances to the total instances.
        * Interpretation for this model - An accuracy score of 1.00 for healthy loans indicates that the model correctly predicted nearly all healthy loans. Similarly, an accuracy score of 0.89 for high-risk loans suggests that the model correctly predicted a high percentage of high-risk loans.
    *Precision:
        * General Description - Precision measures the proportion of correctly predicted positive instances (true positives) out of all instances predicted as positive (true positives + false positives).
        * Interpretation for this model - A precision score of 1.00 for healthy loans indicates that almost all loans predicted as healthy were actually healthy. For high-risk loans, a precision of 0.84 means that 84% of the loans predicted as high-risk were actually high-risk.
    *Recall:
        * General Description - Recall (also known as sensitivity) calculates the proportion of correctly predicted positive instances (true positives) out of all actual positive instances (true positives + false negatives).
        * Interpretation for this model - A recall score of 0.99 for healthy loans implies that the model captured 99% of all actual healthy loans. Similarly, a recall of 0.94 for high-risk loans indicates that the model identified 94% of all actual high-risk loans.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?

    Only one model was evaluated: logistic regression. Evaluation of the performance was done using the confusion matrix and classification reports.

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

    In this exercise, the performance of the model does depend on what we are trying to predict. For predicting healthy loans, the model has perfect precision (1.00) and high recall (0.99), indicating that it correctly identifies almost all healthy loans and rarely misclassifies them. This is crucial for minimizing false positives in this category. However, for predicting high-risk loans, the model has slightly lower precision (0.84), but still has good recall (0.94), resulting in a balanced F-score of 0.89. This means that while it correctly identifies most high-risk loans, there is a slightly higher chance of false positives in this category.

