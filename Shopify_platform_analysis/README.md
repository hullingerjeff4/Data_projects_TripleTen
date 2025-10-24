# 🛍️ Shopify App Marketplace Analysis (Power BI)

This business intelligence project analyzes publicly scraped Shopify App Store data to uncover what makes apps successful on the platform. Using Power BI, DAX, and visual analytics, this report explores marketplace trends, user sentiment, developer responsiveness, and review quality across thousands of apps.

---

## 🎯 Project Goal

**Primary Question:**  
What key factors contribute to the success of a Shopify app?

This project evaluates:
- Review velocity and update frequency
- Correlation between popularity and satisfaction
- Impact of helpful reviews
- Developer responsiveness
- Category-level patterns

Each numbered section of the project corresponds to a visual page in Power BI.

---

## 📂 Dataset Overview

The dataset (`shopify.xlsx`) contains publicly available, web-scraped data from Shopify App Store listings. It includes four tables:

| Table | Description |
|--------|-------------|
| `apps` | App metadata, developer name, ratings, review count, last updated date |
| `reviews` | User ratings/comments, helpful votes, developer responses |
| `categories` | Master list of marketplace categories |
| `apps_categories` | Join table mapping apps to multiple categories |

This relational structure enables multi-dimensional analysis of app success.

---

## 🧠 Tools & Skills Demonstrated

- Power BI Desktop
- DAX calculations
- Data modeling (relationships & cardinality)
- KPI cards & comparative visualizations
- Line charts, scatterplots, bar charts
- Insight annotation & storytelling
- Visual-level filtering for outlier handling

---

## 📊 Part 1 — App Landscape

A new page titled **App Landscape** was created to explore basic marketplace mechanics.

### ✅ Unique App Count (KPI Card)
Counts distinct application IDs to estimate platform size.

### ✅ Review Trends (Line Chart)
- X-axis: `lastmod` (non-hierarchy date)
- Y-axis: `SUM(reviews_count)`
This shows marketplace activity volume and update velocity over time.

### ✅ Popularity vs. Quality (Scatterplot)
- X-axis: `reviews_count`
- Y-axis: `avg_rating`
An annotated interpretation discusses whether high volume correlates with high satisfaction.

---

## 💬 Part 2 — Review Quality & Developer Responsiveness

A new page titled **Reviews** was created to analyze sentiment rigor.

### ✅ Helpful Review Score (DAX Calculated Column)

    helpful_reviews = rating * (1 + helpful_count)

This weights reviews based on how many users marked them “helpful.”  
A KPI card displays the average helpful score.

### ✅ Developer Answer Flag (DAX Calculated Column)

    developer_answered = IF(NOT(ISBLANK(developer_reply)), 1, 0)

This binary metric allows analysis of how developer communication affects satisfaction.

### ✅ Scatterplot — Rating vs. Developer Answering
- X-axis: `developer_answered`
- Y-axis: `avg_rating`

**Insight:** Responsive developers tend to earn better overall user sentiment.

---

## 🧵 Part 3 — App Reviews & Developer Benchmarking

A page titled **App Reviews** was added to benchmark developers.

### ✅ Data Model Relationship
Created a **many-to-one** join:

| From (`Reviews`) | To (`Apps`) |
|------------------|-------------|
| `app_id` | `id` |

This unlocks joined developer-level insights.

### ✅ Developer Rating Totals (Bar Chart)
- X-axis: `developer`
- Y-axis: `SUM(rating)`

**Limitation:** Volume bias — many low ratings inflate totals.

### ✅ Developer Helpful Ratings (Bar Chart)
- X-axis: `developer`
- Y-axis: `AVG(helpful_reviews)`

A more accurate comparison based on sentiment quality.

### ✅ Most Responsive Developers (Bar Chart)
- X-axis: `developer`
- Y-axis: `developer_answered`
- Visual filter: `reviews_count > 500`

This isolates statistically reliable engagement metrics.

---

## 🧭 Key Insights

- High review helpfulness correlates with stronger user sentiment.
- Developer responsiveness is associated with higher average ratings.
- Review totals alone can be misleading — weighted metrics are more useful.
- Filtering high-volume developers reduces noise in comparison.

---

## 🚀 Recommendations

- Track developer responsiveness as a quality KPI.
- Prioritize review helpfulness over raw star counts.
- Consider developer engagement as a ranking factor in app listings.
- Weight category benchmarking by helpful review averages rather than totals.

---

**Author:** Jeffrey Hullinger  
**Role:** Data Analyst  
**Project:** Shopify platform analysis — BI Analytics Portfolio Project  
**Date:** 2025  
