# 🍽️ Zomato Restaurant Business Performance Analysis (BI Analytics)

This business intelligence project analyzes restaurant performance, customer behavior, order volume, and menu profitability on the Zomato platform. Using multi-table relational data, this analysis identifies which restaurants are most popular, which generate the highest revenue, and why certain restaurants outperform others.

---

## 🎯 Project Objective

**Primary Question:**  
What drives restaurant success and revenue performance on Zomato?

Supporting objectives:
- Identify top-performing restaurants
- Understand order volume patterns
- Analyze menu-level profitability
- Compare customer purchasing behavior

---

## 📂 Dataset Overview

The project utilizes five tables provided in the dataset:

| Table | Description |
|--------|-------------|
| `restaurant` | Restaurant details (name, rating, type, etc.) |
| `menu` | Items offered by restaurants and associated pricing |
| `orders` | Transactions placed by customers (restaurant_id, food_id, quantity, total cost) |
| `users` | User/customer demographic information |
| `food` | Food item metadata (category, cuisine, type) |

By joining these tables, we can calculate:
- Total revenue per restaurant
- Order frequency and volume
- Menu category popularity
- Customer segmentation patterns

---

## 🧠 Tools & Skills Demonstrated

- BI Analytics & KPI tracking
- SQL-style relational analysis (joins, aggregates)
- Revenue modeling
- Customer behavior segmentation
- Performance ranking
- Data storytelling & presentation formatting

---

## 🔍 Key Questions Explored

### ✅ **1. Which restaurants are most popular?**
Popularity measured by:
- Total number of orders
- Unique customer count
- Repeat orders

### ✅ **2. Which restaurants generate the highest revenue?**
Calculated by summing order totals across all transactions.

### ✅ **3. What menu items drive revenue?**
Analysis focused on:
- Contribution margin per item
- Quantity sold
- Category-level performance (e.g., fast food vs. fine dining)

### ✅ **4. Why do some restaurants outperform others?**
Drivers include:
- Cuisine type
- Menu diversity
- Price competitiveness
- Customer loyalty
- Restaurant rating and reputation

---

## 📊 Analytical Approach

1. **Aggregate revenue per restaurant** using `orders` and `menu` joins.
2. **Rank restaurants** by:
   - Total revenue
   - Total order volume
   - Number of unique users
3. **Segment customers** by ordering frequency from the `users` table.
4. **Analyze food categories** using the `food` table.
5. **Evaluate menu pricing strategy** by comparing cost vs. demand.

---

## 🧾 Insights Discovered

- Restaurants offering popular cuisine categories tend to generate significantly higher revenue.
- High-rated restaurants attract larger repeat customer bases.
- Certain menu items drive outsized revenue due to high frequency of orders.
- Customer demographics influence ordering behavior and restaurant popularity.

---

## 📈 Business Recommendations

- Promote and feature high-performing cuisine categories.
- Optimize pricing strategy based on demand elasticity.
- Encourage customer retention with targeted loyalty incentives.
- Expand menu variety in categories demonstrating rapid growth.

---

**Author:** Jeffrey Hullinger  
**Role:** Data Analyst  
**Project:** Zomato restaurant analysis — BI Analytics Portfolio Project  
**Date:** 2025  
