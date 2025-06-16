🧠 Task 3: Customer Churn Prediction – Bank Customers

🎯 Objective
The goal of this task is to predict whether a bank customer is likely to leave (churn) using machine learning techniques. This includes preparing and encoding data, building a classification model, and analyzing which features most influence churn.

📁 Dataset
Name: Churn Modelling Dataset
Source: Kaggle - Churn Modelling Dataset
File Used: Churn_Modelling.csv

📊 Features Overview
Feature	Description
CustomerId, RowNumber, Surname: Identifiers (Removed)
CreditScore, Age, Tenure: Customer profile
Balance, NumOfProducts, HasCrCard, IsActiveMember: Bank usage info
EstimatedSalary:	Income
Geography, Gender:	Categorical features (encoded)
Exited: Target (1 = Churned, 0 = Retained)

🧪 Steps Performed
🔹 1. Data Cleaning & Preparation
Loaded dataset using pandas
Dropped irrelevant columns: RowNumber, CustomerId, Surname
Checked for null/missing values (none found)

🔹 2. Categorical Encoding
Gender: Encoded using LabelEncoder (Male → 1, Female → 0)
Geography: Encoded using OneHotEncoding with drop_first=True

🔹 3. Feature Scaling
Standardized numerical features using StandardScaler to improve model convergence

🔹 4. Splitting the Data
Split into 80% training and 20% testing sets using train_test_split

🤖 Model Building
🏷️ Classifier Used: RandomForestClassifier

from sklearn.ensemble import RandomForestClassifier
model = RandomForestClassifier(random_state=42)
model.fit(X_train, y_train)

🔍 Evaluation Metrics

from sklearn.metrics import accuracy_score, confusion_matrix, classification_report
Accuracy: Calculated with accuracy_score
Confusion Matrix: Visualized using confusion_matrix
Classification Report: Displayed precision, recall, f1-score

🔎 Feature Importance
Used .feature_importances_ to determine which features influenced the model most:

import matplotlib.pyplot as plt
pd.Series(model.feature_importances_, index=X.columns).sort_values(ascending=False).plot(kind='bar')
plt.title('Feature Importance')
plt.show()
🏆 Top Influential Features (may vary slightly):
Age
Balance
EstimatedSalary
NumOfProducts
IsActiveMember
CreditScore

📌 Skills Practiced
Skill	Description
✅ Data Cleaning:	Dropping, inspecting nulls
✅ Label & One-Hot Encoding:	For categorical features
✅ Feature Scaling:	For uniform feature treatment
✅ Classification Modeling:	Random Forest
✅ Model Evaluation:	Accuracy, Confusion Matrix, Report
✅ Feature Interpretation:	Feature importance plot


