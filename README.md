# Payment Gateway Performance & Risk Analytics

**A FinTech Data Analytics Portfolio Project**

## Project Overview

The **Payment Gateway Performance & Risk Analytics** project focuses on analyzing synthetic payment transaction data to evaluate payment gateway performance, understand transaction failures, monitor payment risks, and assess financial performance.

The objective is to transform raw transaction data into meaningful business insights that can help understand payment operations, identify performance gaps, and support data-driven business decisions.

This project follows an end-to-end analytics workflow using Python, SQL, and Power BI.

---

## Business Objectives

The key business objectives of this project are:

- Evaluate payment gateway performance and transaction success rates.
- Identify major reasons behind payment failures.
- Compare system-side and customer/bank-side failures.
- Analyze transaction risk scores and chargeback patterns.
- Measure Merchant Discount Rate (MDR) fee revenue.
- Compare MDR fee revenue with chargeback exposure.
- Analyze settlement and refund-related performance.
- Generate actionable business insights and recommendations.

---

## Dataset Information

### Dataset Type: Synthetic Payment Transaction Data

This project uses a **synthetic payment transaction dataset** designed to simulate payment gateway operations and common business scenarios in the FinTech industry.

The dataset contains transaction-level information related to payments, merchants, gateways, financial metrics, risk indicators, and settlement activities.

### Key Dataset Attributes

| Category | Description |
|---|---|
| Transaction Details | Transaction ID, timestamp and user ID |
| Merchant Information | Merchant name and merchant category |
| Gateway Information | Gateway name and payment method |
| Payment Details | Amount, currency, card network and issuer bank |
| Transaction Status | Successful and failed transactions |
| Failure Analysis | Failure reasons and response time |
| Financial Metrics | Settled amount and MDR fee |
| Risk Analysis | Risk score and chargeback flag |
| Refund Information | Refund status and refund amount |
| Settlement Details | Settlement ID, status and settlement date |

### Dataset Disclaimer

The dataset contains simulated information and does not represent actual customer records, real payment transactions, or confidential financial data from any payment company.

All analytical findings are based on this synthetic dataset and are intended for educational and portfolio demonstration purposes.

---

## Project Workflow & Progress

### Phase 1: Data Cleaning & Exploratory Data Analysis (EDA)

**Status: Completed**

Key activities:

- Initial data inspection and structure analysis.
- Identification and handling of duplicate records.
- Missing value analysis.
- Investigation of unusual transaction amounts.
- Data standardization and preparation.
- Transaction amount distribution analysis.
- Payment status and transaction pattern exploration.
- Exploratory visualizations using Python.

### Phase 2: Business Analysis

**Status: Completed**

Business analysis focuses on answering practical FinTech and payment industry questions.

Key analysis areas:

**1. Payment Gateway Performance**
- Gateway-wise transaction performance.
- Successful and failed transaction analysis.
- Gateway success rate comparison.

**2. Transaction Failure Analysis**
- Failure reason distribution.
- System-side vs Customer/Bank-side failures.
- Failed transaction count and amount analysis.

**3. Risk Score & Chargeback Analysis**
- Risk score distribution.
- High-risk transaction analysis.
- Chargeback patterns and financial exposure.
- Risk category-wise chargeback comparison.

**4. MDR Fee Revenue Analysis**
- Total MDR fee revenue.
- Effective MDR rate.
- Chargeback exposure compared with MDR revenue.

**5. Other Payment Business Metrics**
- Transaction performance.
- Settlement-related analysis.
- Refund-related analysis.

### Phase 3: SQL Business Analysis

**Status: Upcoming**

Planned activities using MySQL:

- Transaction-level analysis.
- Gateway-wise performance comparison.
- Merchant and payment method analysis.
- Failure and chargeback analysis.
- Revenue and financial performance analysis.
- Joins, subqueries and Common Table Expressions (CTEs).
- Window functions and advanced analytical queries.

### Phase 4: Power BI Dashboard

**Status: Upcoming**

Planned dashboard components:

- Overall payment performance KPIs.
- Gateway performance dashboard.
- Transaction failure analysis.
- Risk and chargeback monitoring.
- MDR revenue and financial metrics.
- Interactive filters and visualizations.

---

## Tools & Technologies

| Technology | Purpose |
|---|---|
| Python | Data analysis and processing |
| Pandas | Data manipulation and analysis |
| NumPy | Numerical operations and feature creation |
| Matplotlib | Data visualization |
| Seaborn | Statistical data visualization |
| JupyterLab | Interactive development environment |
| MySQL | SQL-based business analysis (upcoming) |
| Power BI | Interactive dashboard development (upcoming) |

---

## Repository Structure

```text
payment-gateway-risk-analytics/
│
├── 01_eda_cleaning.ipynb
│
├── 02_business_analysis.ipynb
│
├── gateway_scorecard.csv
│
├── payment.csv
│
├── payment_cleaned.csv
│
└── README.md
```

### File Descriptions

| File Name | Description |
|---|---|
| `01_eda_cleaning.ipynb` | Data cleaning, preparation and exploratory data analysis |
| `02_business_analysis.ipynb` | Business questions, KPI calculations and analytical insights |
| `gateway_scorecard.csv` | Payment gateway performance summary |
| `payment.csv` | Original synthetic payment transaction dataset |
| `payment_cleaned.csv` | Cleaned payment transaction dataset |
| `README.md` | Project documentation |

---

## Key Business Metrics

The project focuses on evaluating important payment business KPIs, including:

- Total Transactions
- Successful Transactions
- Transaction Success Rate
- Transaction Failure Rate
- Failed Transaction Amount
- Gateway-wise Performance
- High-Risk Transaction Percentage
- Chargeback Rate
- Chargeback Transaction Value
- Total MDR Fee Revenue
- Effective MDR Rate
- Chargeback Exposure as a Share of MDR Revenue

---

## Business Value

This project demonstrates how transaction data can be used to:

- Monitor payment gateway performance.
- Identify major sources of payment failures.
- Understand transaction risk and chargeback exposure.
- Evaluate payment-related fee revenue.
- Support operational and financial decision-making.
- Convert analytical findings into business recommendations.

---

## Current Project Status

| Project Phase | Status |
|---|---|
| Data Cleaning & EDA | Completed |
| Business Analysis | Completed |
| SQL Analysis | Upcoming |
| Power BI Dashboard | Upcoming |
| Final Documentation | In Progress |

---

## Project Goal

The goal of this project is to develop practical FinTech data analytics skills by solving business-oriented problems using transaction data.

It demonstrates the application of data cleaning, exploratory analysis, KPI development, business analysis, and analytical problem-solving in a simulated payment gateway environment.

**Project Status:** Ongoing Portfolio Project
