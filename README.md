# Fraud Detection Analysis
## Overview

### Dataset

The dataset used is Fraud.csv, which contains financial transaction records with the following columns:

step: Unit of time (1 step = 1 hour)

type: Type of transaction (PAYMENT, TRANSFER, CASH_OUT, etc.)

amount: Transaction amount

nameOrig: Customer who initiated the transaction

oldbalanceOrg: Initial balance before transaction

newbalanceOrig: Balance after transaction

nameDest: Recipient of transaction

oldbalanceDest: Recipient balance before transaction

newbalanceDest: Recipient balance after transaction

isFraud: Whether transaction was fraudulent (1) or not (0)

isFlaggedFraud: Whether transaction was flagged as fraud

### Project Structure
Data Loading and Initial Exploration

Import necessary libraries

Load and inspect dataset

Check basic statistics and data information

Data Preprocessing

Handle missing values

Analyze fraud distribution

Examine transaction types and their relationship with fraud

Filter relevant transaction types (CASH_OUT and TRANSFER)

### Feature Engineering

Create new features:

errorBalanceOrig: oldbalanceOrg - newbalanceOrig - amount

errorBalanceDest: newbalanceDest - oldbalanceDest - amount

### Data Analysis

Statistical summary of processed data

Correlation analysis

Fraud pattern identification

### Key Findings
Only CASH_OUT and TRANSFER transaction types contain fraudulent activities

Fraudulent transactions represent a very small portion of the dataset (0.07%)

The dataset is highly imbalanced, which is common in fraud detection problems

Feature engineering reveals balance discrepancies that may help identify fraud

### Technologies Used
Python

Pandas

NumPy

Matplotlib

Seaborn

Google Colab

### Usage
Upload the Fraud.csv dataset to your environment

Run the notebook cells sequentially

The processed data (df2) is ready for machine learning modeling


Model evaluation and interpretation

Deployment of fraud detection system

Note
The dataset is highly imbalanced, which is typical for fraud detection problems. Special consideration should be given to evaluation metrics (precision, recall, F1-score) rather than accuracy alone.
