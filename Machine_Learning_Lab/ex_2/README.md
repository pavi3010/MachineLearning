# Experiment 2: Binary Classification using Naïve Bayes and K-Nearest Neighbors

## Aim and Objective
To implement and evaluate Naïve Bayes (Gaussian, Multinomial, and Bernoulli) and K-Nearest Neighbors (KNN) classifiers for a binary classification problem. The project focuses on:
- Identifying spam emails using the Spambase dataset from Kaggle.
- Evaluating performance using multiple metrics (Accuracy, Precision, Recall, F1 Score, and Specificity).
- Analyzing model behavior regarding overfitting, underfitting, and the bias-variance trade-off.

## Dataset Description
The **Spambase dataset** is a benchmark dataset for identifying spam emails. It contains:
- **4601 entries** with **58 columns**.
- Numerical features extracted from email content.
- A binary class label (1 for spam, 0 for non-spam).

## Preprocessing Steps
1. **Data Loading**: Loaded via Pandas.
2. **Splitting**: Performed a stratified train-test split (80% training, 20% testing).
3. **Scaling**: Applied `StandardScaler` for KNN and Gaussian/Bernoulli NB, and `MinMaxScaler` for Multinomial NB.

## Implementation Details
- **Naïve Bayes**: Implementation of Gaussian, Multinomial, and Bernoulli variants.
- **KNN**: Implemented a baseline classifier and tuned hyperparameters (k-neighbors, weights, and search algorithms) using `GridSearchCV` and `RandomizedSearchCV`.
- **Search Algorithms**: Comparison between KDTree and BallTree for neighbor searching.

## Performance Summary

### Naïve Bayes Metrics
| Metric | Gaussian NB | Multinomial NB | Bernoulli NB |
| :--- | :--- | :--- | :--- |
| Accuracy | 0.8339 | 0.8958 | 0.9012 |
| Precision | 0.7178 | 0.9349 | 0.9024 |
| Recall | 0.9532 | 0.7906 | 0.8402 |
| F1 Score | 0.8189 | 0.8567 | 0.8702 |

*Performance data sourced from experiment results.*

### KNN Tuning Results
- **Optimal k**: 15
- **Best Parameters**: $k=15$, distance weights, using KDTree/BallTree
- **Best CV Accuracy**: 0.9209

## Key Observations
- **Model Comparison**: Tuned KNN models achieved higher accuracy than Naïve Bayes, though Naïve Bayes was more computationally efficient.
- **Computational Efficiency**: BallTree proved more efficient for prediction (0.1619s) compared to KDTree (0.2356s) in this dataset.
- **Bias-Variance**: Naïve Bayes showed higher bias due to feature independence assumptions, while KNN exhibited higher variance at low $k$ values.
