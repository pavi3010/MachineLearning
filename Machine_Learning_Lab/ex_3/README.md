# Regression Analysis using Linear and Regularized Models

This assignment implements and evaluates various regression techniques to predict loan sanction amounts based on customer and property data. It compares a baseline Linear Regression model with regularized models (Ridge, Lasso, and Elastic Net) to analyze model robustness and generalization.

## Objective

To implement linear and regularized regression models for predicting a continuous target variable, evaluate their performance using multiple metrics, visualize model behavior, and analyze overfitting, underfitting, and bias-variance characteristics.

## Dataset

The assignment uses a real-world dataset related to loan applications.

- **Target Variable**: Loan Sanction Amount (USD)
- **Features**: Includes numerical and categorical data such as Age, Income, Income Stability, Profession, Credit Score, and Property Price.
- **Source**: Kaggle: Predict Loan Amount Data

## Implementation Steps

### 1. Data Preprocessing
- **Feature Selection**: Dropped irrelevant identifiers like Customer ID, Name, and Property ID.
- **Missing Value Handling**: Handled missing values by removing records with missing targets and imputing other features using median values for numerical columns.
- **Encoding**: Categorical variables (e.g., Gender, Profession, Location) were transformed using LabelEncoder.
- **Standardization**: Numerical features were standardized to ensure regularization penalties are applied uniformly.

### 2. Exploratory Data Analysis (EDA)
Visualizations were used to understand the data distribution:
- **Target Distribution**: Histograms of "Loan Sanction Amount" to identify data spread.
- **Categorical Analysis**: Count plots for "Income Stability", "Profession", and "Location" to understand applicant demographics.

### 3. Model Implementation
Four regression models were implemented and compared:
- **Linear Regression**: Served as the baseline model.
- **Ridge Regression**: Used to reduce coefficient magnitudes and stabilize the model.
- **Lasso Regression**: Performed automated feature selection by driving some coefficients to zero.
- **Elastic Net**: Combined penalties from both Ridge and Lasso for balanced regularization.

## Conclusion

The assignment demonstrated that while Linear Regression provides a simple baseline, regularization techniques like Ridge and Lasso are essential for improving predictive robustness by controlling model complexity and reducing the risks of high variance and overfitting.
