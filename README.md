
# Financial Fraud Detection Dashboard

### Dashboard Link : https://app.powerbi.com/groups/me/reports/94ba12d9-d4f0-4546-867a-4b4acb45ed97/4e771bec01578d080ebc?experience=power-bi

## Problem Statement

The goal of this project is to analyse a dataset containing financial transactions from a simulated banking environment. Using Power BI, this dashboard helps visualize transaction behavior and detect potentially fraudulent activities based on type, time, and transaction amount. It provides insights into high-risk patterns to support financial fraud monitoring.

## Dataset Overview

The dataset simulates 30 days of banking transactions and includes the following columns:

•	<ins>step</ins> – Time unit (1 hour per step, 744 total steps for 30 days).

•	<ins>type</ins> – Transaction type (CASH_IN, CASH_OUT, TRANSFER, PAYMENT, DEBIT).

•	<ins>amount</ins> – Transaction amount in local currency.

•	<ins>nameOrig</ins> – Account initiating the transaction.

•	<ins>oldbalanceOrg</ins> – Balance before transaction (origin account).

•	<ins>newbalanceOrig</ins>– Balance after transaction (origin account).

•	<ins>nameDest</ins> – Recipient account.

•	<ins>oldbalanceDest</ins> – Balance before transaction (destination account).

•	<ins>newbalanceDest</ins> – Balance after transaction (destination account).

•	<ins>isFraud</ins>– 1 if fraudulent, 0 if not.

•	<ins>isFlaggedFraud</ins> – 1 if flagged due to amount > 200,000.

## Steps Followed

**Step 1: Data Import**

•	Loaded the dataset into Power BI in CSV format.

•	Verified columns and data types.

**Step 2: Data Preparation**

•	Cleaned the data by checking for nulls and duplicates.

•	Ensured numeric columns were in proper format.

•	Added basic formatting for clarity in visuals.

## Dashboard Visuals

**1. Count and Sum of Amount by Transaction Type**

####	Bar Chart (Count) shows most transactions are:

- CASH_OUT (~2.17M)

-	PAYMENT (~2.10M)

####	Line Chart (Sum) shows highest transaction amount in:

-	TRANSFER (~470B)

-	CASH_OUT and CASH_IN also contribute significantly.

**2. Fraud Distribution**

####	Donut Chart indicates:

-	99.87% transactions are non-fraudulent.

-	Only 0.13% (~8.3K) are fraudulent.

**3. Trend of Fraudulent and Non-Fraudulent Transactions Over Time**

####	Line Chart by step shows:

-	Fraudulent activity spikes at multiple time intervals.
-	Most steps have 0 fraud, but certain periods show higher volume (e.g., 51K, 46K counts).

**4. Fraudulent Transactions by Type**

####	Horizontal Bar Chart:

-	Fraud occurs only in TRANSFER and CASH_OUT.

-	No fraud in PAYMENT, CASH_IN, or DEBIT.

**5. Step Count, isFraud Sum, and Amount by Type**

###	This visual combines:

-	Step counts

-	Fraud counts (isFraud)

-	Total amount per type

•	CASH_OUT and TRANSFER dominate in fraud count and amount.

**6. Sum of Amount by Type and Fraud Status**

####	Stacked Bar Chart shows:

-	Fraudulent TRANSFER transactions: ~0.46T

-	Fraudulent CASH_OUT transactions: ~0.38T

-	Other transaction types have no fraud (0T).

 ## Key Insights

1.	CASH_OUT and TRANSFER are the only transaction types associated with fraudulent behavior.

2.	Fraudulent transactions have very high amounts, indicating large-scale fund movement.

3.	Majority of transactions are legitimate, but the small percentage of fraud involves large monetary values.

4.	Fraud occurs in short bursts during specific time windows (visible in trend chart).

5.	No fraudulent activity is observed in PAYMENT, CASH_IN, or DEBIT transaction types.

## Conclusion

The Power BI dashboard effectively highlights patterns in transaction behavior and identifies key fraud trends. By focusing on transaction type, volume, and time, the dashboard pinpoints where fraud is likely to occur. This helps in better monitoring and implementing targeted fraud detection rules—especially in TRANSFER and CASH_OUT transactions.




# Snapshot of Dashboard 
![Image](https://github.com/user-attachments/assets/db629ff8-2f95-412c-887a-fb3fdf12b681)



