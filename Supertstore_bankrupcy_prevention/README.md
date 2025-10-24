# 📊 Superstore Bankruptcy Prevention — Data Visualization & Profitability Optimization

This business intelligence visualization project analyzes profitability patterns, product performance, advertising opportunities, and return behavior for a struggling superstore. Using dashboard-style visualizations, the project identifies what to keep, what to stop selling, and where additional investment (such as advertising) can generate stronger returns.

---

## 🎯 Project Goals

This project answers four strategic questions:

1. **Which data dimension pairs drive the biggest profit and the biggest loss?**
2. **Which products and subcategories should be discontinued or prioritized?**
3. **Which state-and-month combinations are worth advertising in?**
4. **Which products, customers, or dimensions show abnormal return behavior?**

The goal is to use visuals to justify data-driven recommendations that prevent the superstore from going bankrupt.

---

## 🧠 Tools & Techniques

- Data Visualization (charts, graphs, comparative visuals)
- Visual storytelling for business recommendations
- LEFT JOIN prep for returns analysis
- Calculated fields for return rates
- Profitability trend analysis
- Advertising ROI modeling
- Return on Ad Spend (ROAS) thresholds

---

## 🏛️ Dataset Structure

This project uses two main tables:

| Table | Description |
|-------|-------------|
| `Orders` | Products, customers, regions, profit, ship mode |
| `Returns` | Products returned to the store |

A `LEFT JOIN` is used to enrich order records with return behavior.

---

## 📍 Part 1 — Profit & Loss Analysis

To keep the superstore solvent, we first identify:

### ✅ Biggest Profit Centers
Using pairs of dimensions (e.g., `subcategory + region`, `product ID + shipping mode`), visual analysis uncovers:

- High-margin product categories
- Regions where products consistently outperform
- Items that drive repeat profitability

### ❌ Biggest Loss Makers
Visualizations highlight:

- Product categories with persistent negative profit
- Shipping modes that erode margin
- Products with large return-driven losses

### 🚫 Products to Stop Selling
An individual product visualization reveals the most consistently unprofitable SKUs, recommending discontinuation.

### 🎯 Subcategory Prioritization
Three subcategories are recommended to:

- Focus on (high profit)
- Discontinue (high loss, return-heavy)

Business justification is provided visually.

---

## 📣 Part 2 — Advertising Opportunity Analysis

Advertising effectiveness relies on:

- **Geography:** State-level purchasing behavior
- **Timing:** Seasonal trends

This project identifies the **three best state+month combinations** for targeted advertising.

### Visualization Outputs
- Average monthly profit per state
- Seasonal peaks
- Comparative charts across states

### 💵 Willingness to Spend on Advertising
A simple rule was applied:

> *Spend up to 1/5 of profit generated (Return on Ad Spend ≈ 5:1)*

This helps leadership allocate marketing budget confidently.

---

## 🔁 Part 3 — Returned Merchandise Insights

The Returns table is LEFT JOINED onto Orders to classify each purchase:

| Returned | Meaning |
|----------|---------|
| `Yes` | Product was returned |
| `null` | Product was kept |

A calculated field converts:
- `Yes → 1`
- `null → 0`

### 📈 Visualizations Include:
1. **Products with the highest return rate**
2. **Customers with the highest return rate**
3. **Average profit vs. average return rate** by chosen dimension (e.g., shipping mode, state, subcategory)

### 🔍 Risk-Adjusted Recommendation
A scatterplot shows which segments generate:

- High profit with **low** return rate → keep & promote
- Low profit with **high** return rate → discontinue or flag

---

## ✅ Key Insights & Recommendations

- Targeted advertising should focus on high-profit seasonal months for specific states.
- Several product subcategories bleed profit and should be deprioritized.
- Return-heavy SKUs and customers materially damage profitability.
- Shipping modes influence both profit and likelihood of return.
- Visual patterns uncovered systemic inefficiencies contributing to bankruptcy risk.

---

## 🧾 Deliverables

This project includes:

- Profit & loss visuals
- Product discontinuation visual
- Subcategory focus vs. deprioritization visual
- Advertising ROI visualization
- Return rate dashboards (product & customer level)
- Profit vs. return scatterplot

All visuals are tied to business recommendations.

---

## 🛠️ Skills Demonstrated

| Skill Category | Application |
|----------------|-------------|
| Data Visualization | Bar/line/scatter plots, comparative charts |
| Data Modeling | Join operations, calculated return fields |
| Profitability Analytics | Loss tracing, margin evaluation |
| Product Strategy | SKU and subcategory rationalization |
| Marketing Analytics | Seasonal ROI forecasting |
| Risk Analysis | Return-based performance evaluation |
| Executive Storytelling | Visual justification & narrative insights |

---

## 🚀 Future Enhancement Opportunities

Potential next steps include:

- Customer lifetime value modeling (LTV)
- Predictive return risk
- Shipping cost optimization
- Automated SKU profitability labeling
- Regional marketing attribution

---

**Author:** Jeffrey Hullinger  
**Role:** Data Analyst  
**Project:** Superstore bankrupcy prevention — BI Analytics Portfolio Project  
**Date:** 2025  
