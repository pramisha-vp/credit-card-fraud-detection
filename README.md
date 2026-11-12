# Credit Card Fraud Detection & Transaction Drift Analysis

## Project Overview

This project focuses on detecting fraudulent credit card transactions using supervised machine learning techniques. It covers binary classification for fraud detection, multiclass classification for fraud type identification, and temporal analysis of transaction patterns to examine potential data drift.

The project also includes exploratory data analysis, feature investigation, and data leakage assessment as part of the modelling workflow.

## Objectives

- Explore transaction data and identify patterns associated with fraudulent activities.
- Investigate potential data leakage and transaction-time feature eligibility.
- Develop machine learning models for binary fraud classification.
- Perform multiclass classification to identify different fraud types.
- Analyze changes in transaction patterns across different time periods.

## Technology Stack

- **Programming Language:** Python
- **Environment:** Google Colab
- **Data Manipulation:** Pandas, NumPy
- **Data Visualization:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-learn

## Project Workflow

### 1. Data Understanding and Preprocessing

- Dataset structure and data type inspection
- Missing value and duplicate record analysis
- Descriptive statistical analysis
- Data quality checks

### 2. Exploratory Data Analysis (EDA)

- Univariate and bivariate analysis
- Comparison of fraudulent and non-fraudulent transactions
- Transaction amount analysis based on fraud status
- Fraud rate analysis across merchant categories
- Analysis of fraud patterns by transaction hour, day of the week, and weekend status
- Fraud analysis across transaction channels and card-present status

### 3. Feature Analysis and Data Leakage Investigation

- Identification of potential data leakage variables
- Exclusion of transaction and entity identifier columns
- Investigation of transaction-time feature eligibility
- Selection of suitable predictor variables for model development

### 4. Binary Classification

Developed three supervised machine learning models to classify transactions as fraudulent or non-fraudulent:

- Logistic Regression
- Decision Tree
- Random Forest

**Model Performance**

The Decision Tree model achieved the highest accuracy of **99.88%**, with a fraud F1-score of **99.34%**. Random Forest achieved a fraud precision of **100%**, while Logistic Regression achieved an accuracy of **99.00%**.

### 5. Multiclass Classification

Performed multiclass classification using fraudulent transactions to identify different fraud categories.

**Algorithms Used:**
- Logistic Regression
- Decision Tree
- Random Forest

**Model Performance**

Random Forest achieved the best overall performance among the evaluated models, with an accuracy of **96.14%** and a Macro F1-score of **96.40%**.

### 6. Transaction Drift Analysis

Analyzed changes in transaction patterns across different time periods using the drift-related indicators available in the dataset.

The analysis included:

- Monthly transaction volume and fraud rate trends
- Monthly fraud type distribution
- Fraud rate comparison across drift phases
- Transaction amount analysis across drift phases
- Analysis of `concept_drift_score` and `population_shift_index`
- Monthly distribution of `covariate_shift_flag`

The covariate shift analysis showed a notable increase in transactions flagged for shift from April 2026 onwards.

*Note: The drift analysis examines indicators already available in the dataset. Independent statistical drift tests, such as PSI and KS tests, were not implemented.*

## Evaluation Metrics

Model performance was assessed using:

- Accuracy
- Precision
- Recall
- F1-score
- Macro F1-score
- Confusion Matrix
- Classification Report

## Dataset Information

The dataset was provided for project purposes and is not included in this repository due to confidentiality considerations.

## Conclusion

This project demonstrates the application of machine learning techniques to credit card fraud detection and fraud type classification. It also explores transaction behaviour over time through drift-related indicators.

The workflow highlights the importance of exploratory analysis, feature eligibility, data leakage investigation, and model evaluation in developing fraud detection systems.

