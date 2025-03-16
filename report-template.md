# Module 12 Report Template

## Overview of the Analysis

The purpose of this analysis was to evaluate the performance of machine learning models in predicting loan risk levels. Specifically, we aimed to determine whether a loan applicant would be classified as low risk (0) or high risk (1) based on various financial data attributes.

The dataset contained financial information on loan applicants, including historical data points used to assess creditworthiness. Our goal was to predict whether a loan is healthy (0) or high-risk (1) using machine learning.

Key variables in the dataset:
* Target Variable: loan_status (0 = healthy loan, 1 = high-risk loan)
* Features: Various financial indicators such as loan amount, income level, credit history, and other relevant attributes.
* Class distribution: The dataset is highly imbalanced, with 18,765 healthy loans and 619 high-risk loans, which required balancing techniques.

Machine Learning Process:
* Model Selection: Implemented a Logistic Regression model due to its efficiency in binary classification problems.
* Model Training: Trained the model on the training set.
* Evaluation Metrics: Assessed performance using accuracy, precision, recall, and F1-score.


## Results
### Machine Learning Model 1: Logistic Regression

* Accuracy: 99%

* Precision & Recall Scores:

  * Healthy Loans (Class 0):

   * Precision: 1.00

   * Recall: 0.99

   * F1-Score: 1.00

* High-Risk Loans (Class 1):

 * Precision: 0.84

 * Recall: 0.94

 * F1-Score: 0.89

* Confusion Matrix Results:

 * Correctly Predicted Healthy Loans: 18,655

 * Correctly Predicted High-Risk Loans: 583

 * Misclassified Healthy Loans: 110 (classified as high-risk)

 * Misclassified High-Risk Loans: 36 (classified as healthy)

## Summary

* The Logistic Regression model performed well, achieving a high 99% accuracy and excelling in classifying healthy loans with perfect precision and recall.

* However, predicting high-risk loans (class 1) was slightly less accurate, with 84% precision and 94% recall, due to the imbalanced dataset.

* The slightly lower precision for class 1 (0.84) indicates that some loans were misclassified as high risk when they were not.

### Recommendation:

* If correctly identifying high-risk loans is the top priority, further improvement is needed, possibly through advanced resampling techniques or alternative * models like Random Forest or XGBoost.

* If the primary goal is to minimize false negatives for high-risk loans, then recall is the most important metric, and the current model performs well.

Overall, the Logistic Regression model is a strong candidate for predicting loan risk, but there is potential to refine it for better identification of high-risk loans.
