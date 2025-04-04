
# Financial Fraud Detection Dashboard

### Dashboard Link : https://app.powerbi.com/groups/me/reports/94ba12d9-d4f0-4546-867a-4b4acb45ed97/4e771bec01578d080ebc?experience=power-bi

## Problem Statement

The goal of this project is to analyse a dataset related to financial transactions from a simulated banking system. Using Power BI, the objective is to identify key trends, analyze patterns, and detect possible fraudulent activities. This dashboard can help financial institutions understand where fraud typically occurs and implement better fraud detection measures.

# Dataset Overview

The dataset simulates 30 days of transactions and includes the following columns:

•	step: Time step in hours (from 1 to 744 — representing 30 days).

•	type: Type of transaction (e.g., PAYMENT, CASH_OUT, TRANSFER, DEBIT, CASH_IN).

•	amount: Amount of the transaction in local currency.

•	nameOrig: Name of the customer initiating the transaction.

•	oldbalanceOrg: Balance of the origin account before the transaction.

•	newbalanceOrig: Balance of the origin account after the transaction.

•	nameDest: Name of the recipient account.

•	oldbalanceDest: Balance of the destination account before the transaction.

•	newbalanceDest: Balance of the destination account after the transaction.

•	isFraud: Whether the transaction was fraudulent (1 = fraud, 0 = not fraud).

•	isFlaggedFraud: Whether the transaction was flagged as a large transfer (more than 200,000 units).

# Steps Followed
**Step 1: Load Data into Power BI**

•	Imported the dataset (CSV format) into Power BI.

•	Reviewed column names and data types to ensure accuracy.

**Step 2: Data Cleaning and Transformation**

•	Removed null and duplicate values.

•	Ensured that numeric columns (amount, balances) are correctly formatted.

•	Created calculated columns for:
+	Transaction Hour from the "step" column.
+	Balance Difference before and after  transactions for both sender and receiver.

•	Renamed column headers for better readability in visuals.

**Step 3: Creating Visuals**

1. Transaction Types and Volume

•	Bar chart to show the total count of each transaction type.

•	Column chart to display the total amount transacted per type.

•	Pie chart for percentage distribution of transaction types.

2. Fraud vs. Non-Fraud Analysis

•	Donut chart comparing fraudulent vs. non-fraudulent transactions.

•	Bar chart showing number of frauds by transaction type.

•	Time-series chart to show fraud over time (based on the step column).

•	Scatter plot of fraudulent transaction amounts to detect high-value trends.

3. Flagged Transactions

•	Table to highlight transactions flagged as frauds due to high value (>200,000).

•	Bar chart of flagged vs. non-flagged transactions.

4. Account Balance Trends

•	Clustered bar chart comparing old and new balances for origin and destination accounts.

•	Line chart to show how balances change over time during fraudulent transactions.

5. Filters and Interactivity

+	Added slicers for:
+	Transaction type
+	Fraud status
+	Time (steps)
+	Amount ranges

•	Enabled drill-through feature for detailed transaction analysis.

## Key Insights

1.	Fraud occurs mostly in CASH_OUT and TRANSFER transactions.

2.	Most fraudulent transactions have high amounts, often exceeding 100,000.

3.	The majority of transactions are not fraud, but fraudulent ones have higher amounts and sudden changes in account balances.

4.	Flagged transactions (over 200,000) do not always align with actual frauds, highlighting gaps in rule-based systems.

5.	The origin accounts in fraud cases often have sufficient balance, but the destination accounts get emptied post-fraud.

## Conclusion

The Power BI dashboard successfully highlights suspicious trends and high-risk transaction types. These insights can help banks develop stronger fraud detection systems by monitoring transaction type, amount, time patterns, and balance behavior.


# Snapshot of Dashboard 
https://github.com/user-attachments/assets/db629ff8-2f95-412c-887a-fb3fdf12b681



