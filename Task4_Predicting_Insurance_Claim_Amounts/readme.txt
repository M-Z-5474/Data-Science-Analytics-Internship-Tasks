🩺 Task 4: Predicting Insurance Claim Amounts
🎯 Objective
Estimate the medical insurance claim amount (charges) based on personal attributes like age, BMI, smoking status, etc., using a Linear Regression model.

📁 Dataset
Name: Medical Cost Personal Dataset
Source: Kaggle – Insurance Dataset
File: insurance.csv

📌 Problem Type
This is a regression problem since the target variable (charges) is continuous (numeric).

🛠️ Technologies and Libraries Used
- Python
- Pandas
- NumPy
- Seaborn & Matplotlib (for data visualization)
- Scikit-learn (for modeling and evaluation)

📊 Steps Performed

✅ 1. Data Loading and Inspection
Loaded the dataset using pandas.
Inspected structure with .head(), .info(), and .describe().

✅ 2. Data Preprocessing
Applied One-Hot Encoding to categorical features (sex, smoker, region) using pd.get_dummies().
Dropped the original charges column from features.

✅ 3. Feature Visualization
Visualized the impact of important features:
BMI vs Charges
Age vs Charges
Smoker Status vs Charges

Correlation Heatmap
sns.scatterplot(x='bmi', y='charges', hue='smoker', data=df)
sns.scatterplot(x='age', y='charges', data=df)
sns.heatmap(df_encoded.corr(), annot=True)

✅ 4. Model Training – Linear Regression
Split data into training and testing sets (80/20 split).
Trained a Linear Regression model using sklearn.

✅ 5. Model Evaluation
Used the following metrics to evaluate performance:

Metric	Result
MAE (Mean Absolute Error)	4181.19
RMSE (Root Mean Squared Error)	5796.28

These values indicate that the model predictions are on average within ~$4,181 of the actual insurance charges, with some higher deviation as reflected in the RMSE.

📌 Key Skills Demonstrated
Skill	Description
🔹 Data Cleaning	Handled categorical variables via One-Hot Encoding
🔹 Visualization	Plotted feature relationships to understand impact
🔹 Regression Modeling	Applied Linear Regression using Scikit-learn
🔹 Model Evaluation	Used MAE and RMSE to measure model performance

✅ Final Notes
No additional models (like Decision Trees or Random Forest) are required for this task as per the instructions.
The focus was on building a solid baseline regression model and interpreting how features like age, BMI, and smoker status affect insurance costs.


