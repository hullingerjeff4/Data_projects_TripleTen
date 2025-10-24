
# 📦 Superstore Returned Orders Analysis — Storytelling with Data (Tableau)

This data visualization and storytelling project investigates the root causes of returned orders at a national Superstore and builds an interactive Tableau dashboard to help executives reduce return volume, uncover risk patterns, and identify opportunities to improve profitability.

---

## 🎯 Project Objective

**Primary Question:**  
What is causing the high number of returned orders at the Superstore, and how can leadership proactively reduce return volume?

The CEO requested a visual, data-driven explanation and an interactive monitoring dashboard to support decision-making.

---

## 📂 Dataset Overview

This project combines two primary data sources:

| Table | Purpose |
|--------|-----------|
| `Orders` | Product, customer, geographic, sales, and profit data |
| `Returns` | Flags orders that were returned |

A `LEFT JOIN` was applied to enrich each order with a returned/not-returned flag, preserving all original orders.

---

## 🧮 Data Preparation

A calculated field was created to convert the `Returned` column into numeric form:

- `"Yes"` → **1**  
- `null` → **0**

From this:
- **Average** of the field = **Return Rate**
- **Sum** of the field = **Total Returns**

This metric is used consistently across all visualizations.

Additional cleaning included:
- Date aggregation (month, week)
- Customer order count filtering
- Geographic roll-ups (State, City)

---

## 📌 Part 1 — Root Cause Analysis

The following worksheets were developed to explore return behavior across multiple dimensions:

### ✅ 1. Sales vs. Total Returns (Scatterplot)
Aggregated by **Product Subcategory**
- Reveals that high sales volume does **not** always correlate with high returns
- Identifies categories where operational risk increases with scale

### ✅ 2. Return Rate by Product Category (Bar Chart)
- Highlights product categories with systemic return issues
- Enables prioritization for quality review or vendor renegotiation

### ✅ 3. Return-Prone Customers (Filtered Top Customers)
Filter applied:
- Exclude customers with only 1 order
- Identifies habitual return behavior

### ✅ 4. Geographic Return Behavior (Map)
Visualizes return concentration by:
- State
- City
- Region

Helpful for identifying:
- Fulfillment issues
- Shipping damage risks
- Regional preferences

### ✅ 5. Return Rate by Time Period
Monthly or weekly aggregation to detect:
- Seasonal spikes
- Holiday trend impacts
- Promotion-related returns

### ✅ 6. Composite Charts (2)
Two multi-factor views were built, mixing:
- Date
- Geography
- Product category
- Subcategory

These provide multidimensional context for root cause discovery.

---

## 🎛️ Dashboard Design Requirements

A dashboard specification was documented to ensure clear executive utility:

- Display return behavior by:
  - Product category/subcategory
  - Customer segments
  - Geography
  - Time period
- Include interactive filters:
  - Product category
  - Region
  - Date
  - Customer segment
- Provide visual explanations and key takeaways
- Summarize both **Return Rate** and **Total Returns**

This requirement set informs layout, filtering, and story emphasis.

---

## 🧱 Part 2 — Dashboard Construction

### 1. Low-Fidelity Mockups
Created three pen-and-paper dashboard sketches to explore:
- Layout
- Chart priority
- Filter grouping
- Executive readability

### 2. Dashboard Template (Empty Containers)
An empty wireframe was created using:
- Vertical/horizontal containers
- Spacing placeholders
- Reserve zones for KPIs and filters

### 3. Final Dashboard Build
Worksheets were placed into the template and finalized with:
- Titles
- Icons
- Color consistency
- KPI callouts
- Filter interactivity

Both mockups and the completed dashboard were submitted.

---

## 🖥️ Part 3 — Story Presentation (Tableau Story)

A presentation-ready Tableau Story was constructed to:
- Walk executives through return behavior
- Demonstrate dashboard usage
- Recommend actions based on insights

### Story Arc Includes:

#### 🔹 Root Cause Summary
Top drivers of returned orders highlighted visually.

#### 🔹 Measuring Returns
Compared:
- Return Rate (best for comparison)
- Total Number of Returns (best for volume impact)
- Return Cost (best for financial impact)

Each measure is recommended in different contexts.

#### 🔹 Dashboard Overview
Explains:
- Each chart’s purpose
- How to interpret signals
- What action the metric supports

#### 🔹 Demonstration of Usage
Shows how to:
- Apply filters to isolate problem areas
- Drill down from category → subcategory → product
- Flag high-risk geographies and customers

#### 🔹 Recommended Actions
Examples:
- Discontinue or renegotiate high-return SKUs
- Investigate warehouse/shipper issues in problematic geographies
- Create customer return policies for habitual offenders

#### 🔹 Next Steps
- Deploy dashboard organization-wide
- Monitor trends monthly
- Integrate with operations and vendor management

---

## 📈 Key Insights (Examples)

- Certain product categories consistently show elevated return rates
- Seasonal fluctuations suggest promotional or gift-related return spikes
- Specific states exhibit return behavior indicative of shipping damage
- Small set of customers disproportionately drive returns

---

## 🧠 Skills Demonstrated

| Category | Skills |
|----------|--------|
| Data Visualization | Bar charts, scatterplots, maps, composites |
| Data Preparation | LEFT JOIN logic, calculated return fields |
| Storytelling | Executive narrative sequencing |
| Root Cause Analysis | Dimension slicing, filtering, drilldown |
| Dashboard UX | Wireframing, template containers |
| Presentation | Tableau Stories with interactive walkthrough |

---

## 🚀 Opportunities for Future Work

- Model return probability at the SKU level
- Predict shipping damage probability per geography
- Track return reasons text-analytically
- Add return cost to profitability dashboards
- Benchmark vendor-driven issues

---

**Author:** Jeffrey Hullinger  
**Role:** Data Analyst  
**Project:** Superstore returns analysis — BI Analytics Portfolio Project  
**Date:** 2025  
