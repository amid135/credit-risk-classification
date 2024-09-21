# credit-risk-classification

## Overview
The purpose of this project is to analyze historical lending activity and build a machine learning model to assess the creditworthiness of borrowers. Using logistic regression, we aim to predict the likelihood of loan defaults based on various borrower attributes.

## Project Structure
- **Credit_Risk/**: Directory containing the main notebook and data files.
  - **credit_risk_classification.ipynb**: Jupyter notebook for analysis and modeling.
  - **lending_data.csv**: Dataset containing historical lending information.

## Steps Taken
1. **Data Preparation**:
   - Loaded the lending data into a Pandas DataFrame.
   - Created the labels set (`y`) from the `loan_status` column.
   - Constructed the features set (`X`) from the remaining columns.

2. **Data Splitting**:
   - Split the dataset into training and testing sets using `train_test_split`.

3. **Model Creation**:
   - Fitted a logistic regression model using the training data (`X_train` and `y_train`).
   - Made predictions on the testing data (`X_test`).

4. **Model Evaluation**:
   - Generated a confusion matrix to assess prediction accuracy.
   - Printed a classification report detailing precision, recall, and F1 scores for both classes (healthy loans and high-risk loans).

## Model Performance
The logistic regression model effectively predicts both loan statuses. It achieved a high accuracy, indicating strong overall performance. The precision and recall scores for both healthy (0) and high-risk (1) loans were also favorable, suggesting that the model reliably identifies healthy loans while effectively capturing high-risk loans. Overall, the model demonstrates a good balance in performance, making it a suitable tool for assessing credit risk.

## Conclusion
This project successfully developed a logistic regression model to evaluate loan risks based on historical data. Future work may include exploring additional algorithms, feature engineering, and model tuning to enhance predictive performance.


Credit Risk Analysis Report

To evaluate how well the logistic regression model predicts both labels (0 for healthy loans and 1 for high-risk loans), we can analyze the results from the classification report, which includes key metrics such as accuracy, precision, recall, and F1-score for both classes.

Here’s a breakdown of what these metrics mean in this context:

Accuracy: This tells us the overall proportion of correct predictions (both 0s and 1s) out of the total predictions. A high accuracy indicates that the model is effective at distinguishing between healthy and high-risk loans.

Precision:

Precision for 0 (healthy loan): This metric shows the proportion of true healthy loans among all loans predicted as healthy. High precision means that when the model predicts a loan is healthy, it is likely correct.
Precision for 1 (high-risk loan): This measures the proportion of true high-risk loans among all loans predicted as high-risk. High precision here means that the model is reliable in identifying high-risk loans.
Recall:

Recall for 0 (healthy loan): This indicates the proportion of true healthy loans that were correctly predicted. High recall means that the model captures most of the actual healthy loans.
Recall for 1 (high-risk loan): This shows the proportion of actual high-risk loans that were correctly predicted. High recall suggests the model effectively identifies high-risk loans.
F1-score: This is the harmonic mean of precision and recall for each class, providing a balance between them. A high F1-score indicates a good balance of precision and recall.

Summary of Performance
If the model has high accuracy, high precision, and high recall for both classes, it indicates that the logistic regression model is well-suited for predicting loan statuses.
Conversely, if there is a significant imbalance (e.g., high accuracy but low recall for high-risk loans), it suggests that the model may be favoring one class over the other, which could lead to missed detections of high-risk loans.
Final Assessment
After running the classification report, look for:

Values close to 1 for precision and recall indicate strong performance.
A balance between the scores for both classes is ideal.
