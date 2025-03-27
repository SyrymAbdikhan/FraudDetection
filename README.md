
# Fraudulent Transaction Detection Project

This project aims to build a machine learning model to detect fraudulent financial transactions from a given dataset. The goal is to accurately classify transactions as either fraudulent or non-fraudulent based on various features associated with each transaction.

## Dataset

The project utilizes a dataset containing information about financial transactions. The dataset includes features such as transaction amount, type, timestamp, account balance, device type, location, merchant category, and various other numerical and categorical indicators. The dataset also contains a `Fraud_Label` indicating whether a transaction is fraudulent (1) or not (0).

## Steps Taken

The following steps were undertaken in this project:

1.  **Data Exploration:** Initial exploration of the dataset to understand its structure and characteristics.
2.  **Data Cleaning:** Checked for missing values (nulls) and blank strings in the data. No such issues were found.
3.  **Feature Engineering:**
    - Handled the `Timestamp` column by extracting features like hour, day of the week, and month. The original `Timestamp` column was then dropped.
    - Dropped the high-cardinality columns `User_ID` and `Transaction_ID`.
    - Categorical features were encoded using One-Hot Encoding.
    - Numerical features were standardized using StandardScaler.
4.  **Handling Class Imbalance:** The dataset exhibited a class imbalance (more non-fraudulent transactions than fraudulent ones). SMOTE (Synthetic Minority Over-sampling Technique) was applied to the training data to balance the classes.
5.  **Model Selection and Training:** Several classification models were trained and evaluated using cross-validation with hyperparameter tuning:
    * Logistic Regression
    * K-Nearest Neighbors (KNN)
    * Decision Tree
    * Random Forest
    * Gradient Boosting
6.  **Model Evaluation:** The trained models were evaluated on a held-out test set using metrics like F1-score, Precision, Recall, and Confusion Matrix.

## How to Run

1. Install python libraries
    ```bash
    pip install -r requirments.txt
    ```
2. Run the Jupyter notebook following the steps outlined above.
