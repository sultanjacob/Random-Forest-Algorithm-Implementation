# Employee Attrition Prediction using Random Forest Algorithm
This project implements a machine learning solution to predict employee turnover (attrition) using the HR Employee Attrition dataset. The primary goal is to identify at-risk employees and determine the key drivers that lead to resignation.


# Project Objectives

1. Analyze the dataset to find key patterns in employee behavior.


2. Build a Random Forest Classifier to predict the likelihood of an employee leaving.


3. Address Class Imbalance using SMOTE and threshold optimization.



4. Identify Top Drivers of attrition to provide actionable business insights.

# Technical Workflow
1. Data Preprocessing

Target Encoding: The 'Attrition' column was mapped from 'Yes/No' to '1/0'.


Feature Engineering: Dropped irrelevant columns such as EmployeeNumber, EmployeeCount, Over18, and StandardHours.


Categorical Handling: Applied one-hot encoding to convert categorical features into numerical format for the model.


Imputation: Handled missing values using a median strategy to ensure data completeness before modeling.

2. Handling Imbalance
The dataset showed a high imbalance, with significantly more employees staying than leaving.


SMOTE: Applied Synthetic Minority Over-sampling Technique (SMOTE) to the training data to create a balanced dataset (986 samples per class).



Threshold Tuning: Adjusted the decision threshold from 0.5 to 0.3 to increase the model's sensitivity (Recall) toward leavers.

3. Model Performance
After balancing and threshold adjustment, the model achieved:


Overall Accuracy: 81%.



Recall for Leavers: 57%.



Precision for Leavers: 44%.

# Key Business Insights
The Random Forest model identified the following top drivers for employee attrition:

Overtime: Working overtime is the strongest predictor of an employee leaving.

Marital Status (Single): Single employees are more likely to depart than married or divorced peers.

Financial Factors: Stock option levels and monthly income are critical factors in employee retention.

# Conclusion
By implementing SMOTE and lowering the classification threshold, the model effectively shifted from a biased "high accuracy" model to a "high utility" model that identifies 57% of potential leavers. This allows HR departments to proactively engage with at-risk employees before they resign.
