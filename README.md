# Payment Gateway Performance & Risk Analytics

**A payments analytics portfolio project (Python completed; SQL and Power BI to follow)**

## Business Problem

A payment business wants to know where it actually loses money: failed payments, a weak gateway or payment method, or chargebacks. This project analyses 50,000 synthetic payment transactions to find the biggest profit leak and recommend what to do about it.

## Key Findings

- **Chargebacks are the biggest profit leak.** Chargeback losses (Rs 464.6K) are about 1.9x the MDR fee revenue (Rs 241.8K), leaving a net loss of Rs 222.8K in Jan-Jun 2026.
- **No segment explains payment failures.** Success rate is ~78% and stays flat across gateway (77.0-78.9%), payment method, issuer bank and device.
- **Risk score is a useful warning signal.** Payments with risk score above 60 are ~8% of volume but ~19% of chargebacks (6.76% chargeback rate vs ~2.5% for low and medium risk).
- **Gateways look alike.** Success rate, chargeback rate, fee rate and speed are almost identical, so re-routing traffic will not fix the problem.

## Recommendations

1. Pilot step-up verification (e.g., OTP/3DS) for payments with risk score above 60. Track the high-band chargeback rate, with success rate as a guardrail.
2. Review the 38 payments that were both refunded and charged back (possible double loss).
3. Review pricing and chargeback terms, since chargeback losses are about 1.9x fee revenue.
4. Keep a backup plan for Razorpay, which carries about 40% of fee revenue.

## Data

- **Synthetic** payment transactions dataset: 50,000 raw rows (49,820 after cleaning), 1 Jan - 30 Jun 2026.
- Status split: Success 78.07%, Failed 13.76%, Pending 5.11%, Refunded 3.06%.
- The data contains simulated records only. It does not represent real customers, real payments or any real company. Because it is synthetic, many segment patterns are unusually flat and may not match real-world behavior.

## What Was Done

**Phase 1: Data Cleaning and EDA (completed)**
- Removed 50 duplicate rows and corrupted amount outliers (placeholder values).
- Filled missing categorical values and standardized payment method casing.
- Explored payment status, failure reasons, payment method mix, gateway share and amount distribution.

**Phase 2: Business Analysis (completed)**
- Success rate by gateway, payment method, issuer bank, device, hour and weekday.
- Chargeback rate (on charged payments only), chargeback value and risk-score bands.
- MDR fee revenue, effective MDR rate and chargeback loss compared with fee revenue.
- Gateway scorecard combining volume, success, failure, speed, chargebacks and fee revenue.
- Executive Summary with evidence, impact and recommendations.

**Phase 3: SQL Analysis (upcoming)**
- The same business questions in MySQL: aggregations, CASE WHEN, joins, subqueries, CTEs and window functions.

**Phase 4: Power BI Dashboard (upcoming)**
- One-page executive dashboard based on the gateway scorecard.

## Repository Structure

```text
payment-gateway-risk-analytics/
├── 01_eda_cleaning.ipynb        Data cleaning and EDA
├── 02_business_analysis.ipynb   Business analysis and Executive Summary
├── payment.csv                  Original synthetic dataset
├── payment_cleaned.csv          Cleaned dataset
├── gateway_scorecard.csv        Final gateway scorecard
└── README.md
```

## How to Run

```bash
pip install pandas numpy matplotlib seaborn jupyterlab
jupyter lab
```

Open `01_eda_cleaning.ipynb` first, then `02_business_analysis.ipynb`. Keep the CSV files in the same folder as the notebooks.

## Tools

Python, Pandas, NumPy, Matplotlib, Seaborn, JupyterLab. MySQL and Power BI are planned.

## Limitations

- Synthetic data covering six months only.
- MDR fee is gross, and chargeback penalty fees are not included.
- About 1% of transactions have an Unknown gateway or issuer bank.
- Gateway-level differences in chargeback loss rest on small samples (119-455 chargebacks per gateway) and should not be over-read.

## Project Status

| Phase | Status |
|---|---|
| Data Cleaning and EDA | Completed |
| Business Analysis | Completed |
| SQL Analysis | Upcoming |
| Power BI Dashboard | Upcoming |

## Author

Vijay Rathor | BSc Mathematics | Entry-level Data Analyst
