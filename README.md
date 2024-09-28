# Loan_status_analysis
This code provides a complete workflow for handling, processing, and applying machine learning models on a dataset. Here's a summary of what each part of the code does:

1.Loading the Data: You load the dataset using Pandas and check the first few and last few rows using data.head() and data.tail().

2.Data Exploration:

->You check the shape of the dataset (data.shape) to find out how many rows and columns it has.
->Use data.info() to inspect the columns, data types, and missing values.
->Check for null values using data.isnull().sum().

2.Handling Missing Data:

->You drop the "Loan_ID" column because it’s not useful for predictions.
->You handle missing values in columns like Gender, Dependents, LoanAmount, and Loan_Amount_Term by dropping rows with missing values in certain columns, and using the mode to fill missing values for Self_Employed and Credit_History.

3.Categorical Variable Encoding:

Convert categorical columns (Gender, Married, Dependents, etc.) into numeric values using mapping.

4.Feature Scaling:

You scale the numerical features using StandardScaler from sklearn.

5.Splitting Data:

You create feature matrix X and target vector y and split the dataset into training and testing sets.

6.Model Training and Validation:

->You create a function model_val to train a model, print its accuracy, and compute cross-validation scores.
->You test different classifiers: Logistic Regression, SVC, Decision Tree, Random Forest, and Gradient Boosting Classifier.

7.Hyperparameter Tuning:

->You use RandomizedSearchCV for hyperparameter tuning of Logistic Regression, SVC, and Random Forest classifiers to find the best parameters.

The workflow is designed to provide a complete process from data cleaning to model training, evaluation, and tuning. 
You can now execute this in Google Colab or a local Jupyter notebook to test and optimize these models for the loan prediction dataset.











