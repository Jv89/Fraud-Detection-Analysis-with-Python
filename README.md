# Fraud Detection Analysis with Python

## Project Overview

This project analyzes a financial transactions dataset to identify fraud patterns using Python. The focus is on data exploration, data quality checks, transaction behavior, fraud distribution, and simple business insights.

The goal is not to build a complex machine learning model. Instead, this project is designed to demonstrate a clear beginner-to-intermediate data analysis workflow using `pandas` and basic visualizations.

## Dataset

The original dataset contains online financial transactions with the following fields:

- `step`: Time step of the transaction
- `type`: Transaction type
- `amount`: Transaction amount
- `nameOrig`: Origin account
- `oldbalanceOrg`: Origin account balance before the transaction
- `newbalanceOrig`: Origin account balance after the transaction
- `nameDest`: Destination account
- `oldbalanceDest`: Destination account balance before the transaction
- `newbalanceDest`: Destination account balance after the transaction
- `isFraud`: Fraud label where `1 = fraud` and `0 = not fraud`
- `isFlaggedFraud`: System flag for potentially fraudulent transactions

The full dataset has **6,362,620 transactions** and **11 columns**.

> Note: The full CSV file is too large for a standard GitHub upload. This repository includes a smaller sample dataset for demonstration purposes.

## Tools Used

- Python
- pandas
- matplotlib
- Jupyter Notebook

## Business Questions

This analysis answers the following questions:

1. How many transactions are included in the dataset?
2. What percentage of transactions are fraudulent?
3. Which transaction types are most common?
4. Which transaction types are most associated with fraud?
5. What is the total and average amount involved in fraudulent transactions?
6. How do transaction amounts differ between fraud and non-fraud transactions?
7. How does fraud activity change over time?
8. How often does the system flag transactions that are actually fraudulent?
9. Are there missing values that should be reviewed before deeper analysis?

## Key Findings from the Full Dataset

- The full dataset contains **6,362,620 transactions**.
- There are **8,213 fraudulent transactions**, which represents approximately **0.13%** of all transactions.
- Fraud is highly imbalanced, meaning non-fraud transactions are much more common than fraud transactions.
- Fraud appears only in `TRANSFER` and `CASH_OUT` transaction types in this dataset.
- The total amount involved in fraudulent transactions is approximately **$12.06B**.
- The average fraudulent transaction amount is approximately **$1.47M**.
- Only **16 transactions** were flagged by the system as fraud, while the dataset contains **8,213 actual fraud cases**.
- No missing values were found in the main dataset fields.

## Project Structure

```text
Fraud-Detection-Python-Analysis/
├── README.md
├── data/
│   └── fraud_transactions_sample.csv
└── notebooks/
    └── Fraud_Detection_EDA.ipynb
```

## Skills Demonstrated

- Reading and inspecting CSV data with pandas
- Checking dataset shape, columns, data types, and missing values
- Calculating fraud rate and fraud transaction totals
- Grouping data by transaction type
- Comparing fraud and non-fraud transactions
- Creating basic visualizations with matplotlib
- Communicating findings in a business-friendly way

This project is intentionally focused on exploratory data analysis rather than advanced machine learning. A machine learning model could be added later once the exploratory analysis is stronger and the class imbalance problem is handled properly.
