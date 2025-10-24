# 🛒 E-Commerce User Funnel, Cohort, & Retention Analysis (BI Analytics)

This business analytics project evaluates how effectively an e-commerce website converts user activity into purchases, assigns customers into monthly acquisition cohorts, and measures retention behavior over time. The analysis was completed using spreadsheet-based business intelligence techniques with emphasis on funnel performance, revenue behavior, and retention tracking.

---

## 📌 Project Objectives

This analysis answers three primary business questions:

1. **How well does the website convert product views into purchases?**
2. **What are the monthly acquisition cohorts and how do they behave over time?**
3. **What are customer retention rates over a multi-month period?**

---

## 📂 Dataset Overview

The raw dataset (`raw_user_activity`) contains time-stamped website events:

| Column | Description |
|--------|-------------|
| `user_id` | Unique customer identifier |
| `event_type` | Activity performed by the user |
| `category_code` | Product category |
| `brand` | Product manufacturer |
| `price` | Product price (USD) |
| `event_date` | Date of interaction (YYYY-MM-DD) |

Customer actions include viewing product pages, opening carts, and completing purchases.

---

## 📍 Part 1 — Conversion Funnel

A three-stage conversion funnel was created to measure conversion efficiency:

| Funnel Stage | Definition |
|--------------|------------|
| Product Page View | Customer views an item page |
| Shopping Cart | Customer adds an item to cart |
| Purchase | Customer completes a transaction |

### Techniques Used
- Pivot tables
- **Unique** user counting
- Derived columns:
  - **Total Conversion Rate** (views → purchase)
  - **Step-to-Step Conversion Rate** (cart → purchase)

This funnel reveals where users drop off in the buying journey.

---

## 💳 Part 2 — Data Preparation for Cohort Analysis

To accurately track retention, purchase-only data was isolated.

### Steps Completed
- Filtered purchase events into a `purchase_activity` sheet (4,845 rows after filtering)
- Created pivot table (`first_purchase`) to determine each customer’s earliest purchase
- Created helper columns:

| Column | Purpose |
|--------|----------|
| `first_purchase_date` | VLOOKUP of earliest event per user |
| `event_month` | Month/year of each transaction (`YYYY-MM`) |
| `first_purchase_month` | Cohort assignment month |
| `cohort_age` | Age in months since cohort acquisition (DATEDIF) |

These engineered features enable cohort grouping and retention measurement.

---

## 👥 Part 3 — Cohort Analysis & Retention Rates

Using a pivot table in `cohort_analysis`:

- Cohorts were grouped by **first purchase month**
- Each cohort tracked over **0–4 months**
- Unique active users counted at each age interval

### Retention Calculation

A separate `retention_rates` sheet:

- Displays retention % relative to each cohort’s month-0 population
- Excludes cohort_age 0 (baseline size)
- Uses fixed column references for scalable formulas

This unveils user engagement longevity after acquisition.

---

## 🧾 Part 4 — Executive-Ready Reporting

To deliver a polished, professional spreadsheet:

### ✅ Executive Summary
Includes:
- Funnel summary
- Retention insights
- Assumptions behind data decisions

### ✅ Sheet Organization
Ordered to increase clarity:

1. Table of Contents
2. Executive Summary
3. Analytical Results
4. Calculations
5. Raw Data

### ✅ Formatting Improvements
- Date formatting
- Bold headers
- Cell borders
- Frozen row headers
- Highlighted calculated outputs

These upgrades support readability for leadership stakeholders.

---

## 📊 Key Insights

- A noticeable drop-off occurs between product views and purchases, indicating opportunity for UX optimization.
- New user cohorts show declining activity after several months, highlighting retention challenges.
- Cohorts vary in performance based on acquisition month, suggesting seasonal or marketing influences.

---

## 🧠 BI Skills Demonstrated

| Category | Skills |
|----------|--------|
| Data Cleaning | Filtering, deduplication, date handling |
| Data Modeling | Event funnel construction, cohort segmentation |
| Analytics | Retention calculation, cohort aging logic |
| Spreadsheet Functions | `VLOOKUP`, `TEXT`, `DATEDIF`, fixed references |
| Visualization | Funnel conversion metrics |
| Communication | Executive summary writing, sheet organization |

---

## 🛠️ Tools Used

- Google Sheets / Excel
- Pivot Tables
- Conditional Logic
- Date Functions
- Cohort Tracking Methodology

---

## 🚀 Opportunities for Future Enhancement

If expanded, this analysis could also include:

- Revenue per cohort
- Customer lifetime value (LTV)
- Churn scoring
- Attribution by category/brand
- Funnel optimization A/B testing

---

