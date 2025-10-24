# 🏙️ Manhattan Airbnb Market Analysis (BI Analytics)

A business-intelligence project evaluating Manhattan’s short-term rental market using Airbnb listing and calendar data. The goal is to identify **high-performing neighborhoods**, **optimal property sizes**, and estimate **annual revenue potential** for top-earning listings.

---

## 📌 Project Objectives

This analysis answers two key questions:

1. **Which neighborhoods and property sizes are most attractive for vacation rentals?**
2. **How much money did these listings generate?**

Attractiveness is measured using **reviews from the last 12 months** — a proxy for rental frequency.

---

## 📂 Dataset Overview

| Dataset | Description |
|--------|-------------|
| Listings | Bedrooms, neighborhood, review metrics |
| Calendar | Daily availability & adjusted nightly price |

📎 See project artifact reference at the bottom of this README.

---

## 🧹 Data Cleaning

To ensure reliable analysis:

### ✅ Neighborhood Standardization
- Removed inconsistent capitalization
- Trimmed trailing spaces
- Created `neighborhood_clean` column

### ✅ Bedroom Cleaning
- Empty values treated as **0 bedrooms (studio)**
- Created `bedrooms_clean` using `IF()` logic

### ✅ Raw Data Protection
- Raw sheets duplicated prior to transformation

All cleaning steps documented in a dedicated sheet.

---

## 📊 Most Attractive Neighborhoods

Using a pivot table with:

- **Values:** `number_of_reviews_ltm` (reviews in the last 12 months)
- **Sort:** Descending

The **three most attractive** neighborhoods identified:

- Harlem
- Hell’s Kitchen
- Lower East Side

A bar chart visualizes the top 10.

---

## 🛏️ Most Popular Property Sizes

Bedroom popularity based on listing volume:

| Bedrooms | Listings |
|----------|----------|
| 1-Bedroom | 1,265 |
| 2-Bedroom | 526 |
| Studio (0 BR) | 441 |

✅ **1-bedroom** units are most attractive across Manhattan.

---

## 🏠 Neighborhood Bedroom Preferences

After combining neighborhood + bedroom data:

- All top neighborhoods prefer **1-bedroom** units
- **Midtown** prefers **studios**

Example:
- Harlem’s preferred size: **1-Bedroom**

---

## 🥇 Selecting Top Listings

A field `top_listing` was engineered:

