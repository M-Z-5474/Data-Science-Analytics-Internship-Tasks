Task 5: Personal Loan Acceptance Prediction

Objective:
The goal of this task is to predict which customers are likely to accept a personal loan offer based on their demographic and financial information.

Dataset:
Source: UCI Machine Learning Repository
Name: Bank Marketing Dataset
The dataset includes customer details such as age, job, marital status, education level, and whether the customer accepted the loan offer (target variable: "yes" or "no").

Steps Completed:

Step 1: Data Loading and Exploration
Loaded the dataset using pandas.
Checked the dataset shape, column names, and value types.
Explored key features like age, job, marital status, and education.
Analyzed the target class distribution (most customers did not accept the loan).

Step 2: Preprocessing
Encoded categorical features using Label Encoding and One-Hot Encoding.
Checked for imbalanced classes (yes vs no).
Applied SMOTE (Synthetic Minority Oversampling Technique) to balance the classes.

Step 3: Model Training
Trained two machine learning models:
Logistic Regression
Decision Tree Classifier
Used train_test_split to divide data into training and testing sets.

Step 4: Model Evaluation
Evaluated both models using the following metrics:
Confusion Matrix
Precision, Recall, and F1-Score
Accuracy
Tested model performance before and after applying SMOTE.

Results Summary:
Before Applying SMOTE (Imbalanced Data):
Logistic Regression Results:
Accuracy: ~90%
Precision for "yes": 0.65
Recall for "yes": 0.21
The model struggled to correctly identify customers who accepted the loan.

Decision Tree Results:
Accuracy: ~90%
Precision for "yes": 0.61
Recall for "yes": 0.23
After Applying SMOTE (Balanced Data):

Decision Tree Results:
Accuracy: ~84%
Precision for "yes": 0.34
Recall for "yes": 0.44
F1-Score for "yes": 0.39
SMOTE helped improve recall for customers who accepted the loan offer, even though the overall accuracy slightly dropped.

Business Insights:
Most customers are not interested in personal loan offers.
Due to class imbalance, models tend to favor predicting "no".
After balancing with SMOTE, the model identifies potential loan acceptors more accurately.
This helps the bank target the right group of customers for future campaigns.

Tools and Libraries Used:
Python
pandas and numpy (for data handling)
seaborn and matplotlib (for visualization)
scikit-learn (for model training and evaluation)
imbalanced-learn (for SMOTE)

Files Included:
Task_5_Personal_Loan_Acceptance_Prediction.ipynb (complete code and analysis)
bank_additional_full.csv (dataset)
readme.txt (this documentation)


