# Comparing Classifiers on Bank Marketing Campaign Data

## Overview
This project applies and compares the performance of four machine learning classifiers—Logistic Regression, K-Nearest Neighbors (KNN), Decision Tree, and Support Vector Machine (SVM)—to predict whether a client will subscribe to a term deposit based on features collected from a series of Portuguese bank telemarketing campaigns.

The dataset, sourced from the UCI Machine Learning Repository, contains detailed client information, contact history, and economic indicators. The objective is to optimize telemarketing efforts by identifying the clients most likely to subscribe.

## Business Objective
The goal of this analysis is to build predictive models that accurately determine which clients are likely to respond positively to a marketing campaign. By doing so, financial institutions can improve the efficiency of outreach strategies, reduce campaign costs, and increase client conversion rates.

## Data
- **Source**: UCI Bank Marketing Dataset
- **File Used**: `bank-additional-full.csv` (41,188 rows, 20 input features + 1 target)
- **Target Variable**: `y` (binary: `yes` for subscription, `no` otherwise)

## Methods
The following preprocessing steps and techniques were applied:
- Dropped the `duration` column to avoid data leakage.
- One-hot encoding for categorical variables.
- Train-test split with stratification to preserve target distribution.
- Feature scaling using `StandardScaler` for models sensitive to distance (KNN, SVM, Logistic Regression).

## Models Compared
- **Logistic Regression**
- **K-Nearest Neighbors**
- **Decision Tree Classifier**
- **Support Vector Machine**

Each model was evaluated based on:
- Training and test accuracy
- F1 score and confusion matrix
- GridSearchCV for hyperparameter optimization
- Training time

## Key Findings
- The Decision Tree classifier, after tuning, achieved the highest test accuracy with interpretable rules.
- Logistic Regression performed consistently well and is easily interpretable.
- KNN and SVM required more time to train and were more sensitive to scaling and feature selection.
- Clients with previous successful contacts, or who were contacted in specific months, were more likely to subscribe.

## Recommendations
- Prioritize contacting clients with past campaign engagement and success.
- Refine outreach strategies around favorable time periods (e.g., March and May).
- Use Decision Tree or Logistic Regression in production for their balance of accuracy and interpretability.
