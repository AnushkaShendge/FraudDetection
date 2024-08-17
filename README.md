# Fraud Detection in Financial Payments

This project focuses on detecting fraudulent transactions in financial payments using machine learning. The primary model used in this project is the XGBoost classifier, which achieved an accuracy of **99.97%**.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Data Preprocessing](#data-preprocessing)
- [Modeling](#modeling)
- [Evaluation](#evaluation)
- [How to Run](#how-to-run)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Project Overview
Financial fraud detection is crucial for protecting customers and financial institutions. This project implements a machine learning model to classify transactions as fraudulent or non-fraudulent. The model is trained on a dataset containing millions of transactions, and the final XGBoost model achieved high accuracy, making it a reliable tool for detecting fraud.


![Screenshot 2024-08-18 002333](https://github.com/user-attachments/assets/3bfc52b7-7d41-4ccf-ae92-9e340385c7f8)
![Screenshot 2024-08-18 002424](https://github.com/user-attachments/assets/77cceb81-5c7f-4e0c-a086-94f28eabdcc5)


## Dataset
The dataset used in this project is sourced from [Kaggle](https://www.kaggle.com/). It consists of financial transaction records with the following features:

- **step**: Time step between transactions.
- **type**: Type of transaction (e.g., payment, cash_out, transfer, debit).
- **amount**: Amount of the transaction.
- **nameOrig**: ID of the source account.
- **oldbalanceOrig**: Initial balance before the transaction.
- **newbalanceOrig**: New balance after the transaction.
- **nameDest**: ID of the destination account.
- **oldbalanceDest**: Initial balance of the destination account before the transaction.
- **newbalanceDest**: New balance of the destination account after the transaction.
- **isFraud**: Label indicating whether the transaction is fraudulent (1) or not (0).

**Dataset Statistics:**
- Number of samples: 4,924,927
- Number of features: 10

## Data Preprocessing
### Steps:
1. **Dropping Irrelevant Columns**: Columns like `nameOrig` and `nameDest` were dropped as they are not directly useful for prediction.
2. **Handling Missing Values**: Identified and dropped rows with missing values.
3. **One-Hot Encoding**: Categorical features (like `type`) were encoded using One-Hot Encoding.
4. **Feature Scaling**: Numerical features were scaled to standardize the range.


## Results
- **Accuracy**: 99.97%
- **Precision**: High
- **Recall**: High
- **F1-Score**: High
