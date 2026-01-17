# Indonesia QRIS Payment Behavior & Churn Analysis

This project analyzes user behavior and churn patterns in a digital payment ecosystem, framed within the context of Indonesia’s QRIS (Quick Response Code Indonesian Standard) payment infrastructure.

Using transaction-level data, the analysis examines how different payment rails—QRIS-based payments versus non-QRIS card payments—relate to user engagement, transaction value, and behavioral churn. The goal is to demonstrate end-to-end analytical thinking, from data preparation to business insight generation.

---

## Business Context

QRIS is Indonesia’s unified QR code payment system, enabling payments across banks and e-wallet providers through a single standardized interface. In practice, QRIS payments can be initiated from:
- **Bank-based applications** (mobile banking)
- **Wallet-based applications** (e-wallet balances such as GoPay, OVO, DANA, etc.)

To reflect this ecosystem, raw payment methods in the dataset are recoded into three Indonesia-relevant categories:
- **QRIS (Bank-based)**
- **QRIS (Wallet-based)**
- **Non-QRIS (Cards)**

This recoding is used as an analytical proxy to compare behavioral patterns across payment types.

---

## Churn Definition

This is a non-subscription payment context, so churn is defined behaviorally:

> **A user is considered churned if they have no transactions within the final 90 days of the observation window.**

This approach is commonly used in fintech and e-commerce analytics where explicit cancellations do not exist.

---

## Key Questions

- Do churn rates differ between QRIS-based payments and non-QRIS card payments?
- Is churn driven more by low engagement (frequency) or low transaction value?
- How do usage and churn dynamics evolve over time?

---

## Key Findings

- **Churn is primarily engagement-driven.**  
  Active users complete more transactions on average than churned users, while transaction values remain relatively similar across groups.

- **QRIS-based payments are slightly more “sticky.”**  
  Both bank-based and wallet-based QRIS payments exhibit marginally lower churn rates compared to non-QRIS card payments.

- **Most users are low-frequency users.**  
  The median number of transactions per user is one, indicating that retention improvements are likely driven by small increases in repeat usage rather than the emergence of high-frequency “power users.”

- **Usage patterns are stable over time.**  
  Monthly activity and churn share show limited volatility, suggesting churn reflects ongoing behavioral patterns rather than short-term shocks.

---

## Methods

- Transaction-level exploratory data analysis using **pandas** and **matplotlib**
- Feature engineering to map generic payment rails into QRIS-based categories
- Behavioral churn modeling using a 90-day inactivity window
- User-level engagement and transaction value analysis
- Monthly trend analysis for activity and churn dynamics

---

## Visualizations

All charts are designed using a business-friendly, executive-style aesthetic:
- Clear color semantics (e.g., higher churn highlighted distinctly)
- Minimal visual clutter
- Slide- and dashboard-ready formatting

These visuals are suitable for stakeholder presentations and executive summaries.

---

## Limitations & Assumptions

- The dataset is anonymized and synthetic/public, and does not represent proprietary data from specific Indonesian payment providers.
- Payment method recoding is intended to reflect Indonesia’s QRIS infrastructure for analytical purposes, not to measure exact market shares.
- Churn is inferred behaviorally based on inactivity; alternative churn windows may yield different absolute rates.
- Users may transact using multiple payment methods; simplified user-level aggregation is applied where necessary.

---

## Repository Structure

├── data/
│ └── digital_wallet_transactions.csv
├── analysis.ipynb
└── README.md

---

## Author
**Laksa Fadhil Yansen**  
Data Analyst | Data Science
Python • SQL • R • Data Analytics & Visualization
