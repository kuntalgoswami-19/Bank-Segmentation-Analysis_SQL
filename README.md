# 🏦 Bank Segmentation Analysis

A SQL-based financial analytics project focused on analyzing customer behavior, transaction activity, account usage, and regional banking performance using simulated banking data.

## 📌 Project Overview

This project simulates a retail banking environment and uses PostgreSQL to analyze customer and transaction data.

The objective is to transform structured banking data into meaningful business insights by identifying customer segments, transaction trends, account activity, dormant accounts, and regional performance.

> **Note:** The dataset is simulated and does not contain real customer or banking information.

---

## 🎯 Objectives

The analysis focuses on:

- Identifying high-value customers
- Analyzing customer spending and transaction behavior
- Detecting dormant and underutilized accounts
- Understanding account and product usage
- Analyzing monthly and yearly transaction trends
- Measuring banking performance across cities and regions
- Identifying frequently used transaction services
- Segmenting customers based on account and transaction activity

---

## 🛠️ Tech Stack

- **Database:** PostgreSQL
- **SQL:** CTEs, JOINs, GROUP BY, CASE WHEN, aggregate functions
- **Advanced SQL:** Window Functions, FILTER, DATE_TRUNC
- **Database Tool:** pgAdmin

---

## 🗂️ Database Structure

The project uses three core tables:

### 1. Customers

Contains customer-level information such as:

- Customer ID
- Name
- Gender
- Date of Birth
- City
- Region

### 2. Accounts

Contains account-level information such as:

- Account ID
- Customer ID
- Account Number
- Account Type
- Account/Product information

### 3. Transactions

Contains transaction-level information such as:

- Transaction ID
- Account ID
- Transaction Date
- Transaction Type
- Transaction Amount
- Transaction Description

### Relationship

```text
Customers
    │
    │ Customer_ID
    ▼
Accounts
    │
    │ Account_ID
    ▼
Transactions
```

This relational structure allows customer-level, account-level, and transaction-level analysis.

---

## 🔎 Key Analysis Performed

### 1. Customer Spending Analysis

Calculated total debit/spending amounts for customers to identify high-spending customers.

### 2. Salary Trend Analysis

Analyzed salary-related credit transactions across different months to understand salary payment patterns.

### 3. Most Active Accounts

Identified accounts with the highest:

- Number of transactions
- Total transaction volume

### 4. Monthly Transaction Analysis

Analyzed transaction count and transaction volume by month to understand changes in banking activity over time.

### 5. Yearly Transaction Analysis

Compared transaction activity across years to identify long-term trends.

### 6. High-Value Customer Analysis

Ranked customers based on total credit inflows to identify customers with significant account activity.

### 7. Dormant Account Detection

Identified accounts/customers with no transaction activity during the previous 12 months.

### 8. Single-Product Customer Analysis

Identified customers who use only one account/product type, providing a basis for potential cross-selling analysis.

### 9. Transaction Service Analysis

Analyzed transaction descriptions to identify frequently used banking services such as transfers, POS transactions, salary payments, and utility payments.

### 10. City-Level Performance

Compared transaction volume, customer activity, and account performance across different cities.

### 11. Regional Engagement Analysis

Compared active and dormant customers/accounts across regions to understand geographical differences in engagement.

### 12. Highest Spender by City

Used ranking logic to identify the highest-spending customer within each city.

---

## 🧠 SQL Concepts Demonstrated

This project demonstrates practical use of:

```text
SELECT
WHERE
GROUP BY
HAVING
ORDER BY
CASE WHEN
JOIN
LEFT JOIN
CTE
Aggregate Functions
Window Functions
FILTER
DATE_TRUNC
Subqueries
Ranking
Conditional Aggregation
```

---

## 📊 Business Insights

The analysis can help a banking organization understand:

- Which customers generate the highest transaction value
- Which accounts have the highest engagement
- Where customer activity is concentrated geographically
- Which customers/accounts may be dormant
- Which banking services are most frequently used
- How transaction activity changes over time
- Which customers use only a limited number of banking products

These insights can support customer relationship management, reactivation campaigns, cross-selling analysis, and regional performance analysis.

---

## 📁 Project Files

| File | Description |
|------|-------------|
| `schema_setup.sql` | Creates the database schema and tables |
| `data_generation.sql` | Generates simulated banking data |
| `bank_segmentation.sql` | Contains SQL analysis queries |
| `analysis_case_summary.md` | Documents the analysis, findings, and business interpretation |
| `README.md` | Project documentation |

---

## 🚀 How to Run

### 1. Create the database

Create a PostgreSQL database using pgAdmin.

### 2. Create the tables

Run:

```sql
schema_setup.sql
```

### 3. Generate the data

Run:

```sql
data_generation.sql
```

### 4. Run the analysis

Execute:

```sql
bank_segmentation.sql
```

The queries will generate customer, account, transaction, and regional analysis results.

---

## 📚 Key Learnings

Through this project, I strengthened my ability to:

- Design and query relational banking data
- Combine multiple tables using SQL JOINs
- Perform customer-level and transaction-level aggregation
- Use CTEs and window functions for analytical queries
- Perform time-series analysis using PostgreSQL date functions
- Detect dormant and highly active accounts
- Translate SQL results into business-oriented insights

---

## 👨‍💻 Project Focus

**Data Analytics | SQL | PostgreSQL | Financial Analytics | Customer Segmentation**

This project demonstrates how SQL can be used to transform structured financial data into actionable analytical insights.
