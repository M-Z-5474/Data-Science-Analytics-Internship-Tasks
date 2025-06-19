✅ Task 2: Credit Risk Prediction
🎯 Objective
To predict whether a loan applicant is likely to default on a loan using machine learning techniques.

📁 Dataset
Name: Loan Prediction Dataset

Source: Kaggle – Loan Prediction Problem

🧪 Steps Performed
🧹 Data Cleaning
Checked for missing values using .isnull().sum()

Handled missing data:

Categorical: Filled using mode

Numerical: Filled using median or mode

📊 Exploratory Data Analysis (EDA)
Visualized:

Loan Amount Distribution (Histogram)

Loan Status by Education (Countplot)

Applicant Income vs Loan Status (Boxplot)

🔄 Preprocessing
Encoded categorical variables using LabelEncoder

Scaled features using StandardScaler (for Logistic Regression)

🤖 Model Building
Classification Models:

Logistic Regression (with scaling)

Decision Tree Classifier

Evaluation:

Accuracy Score

Confusion Matrix with ConfusionMatrixDisplay

🧠 Skills Practiced
Data cleaning & preprocessing

Exploratory Data Analysis (EDA)

Binary classification using:

Logistic Regression

Decision Tree

Model evaluation using:

Accuracy

Confusion Matrix

