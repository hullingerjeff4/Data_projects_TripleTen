# 🚀 Venture Insights — BI Analytics Project

Welcome to **Venture Insights**, a business intelligence and analytics project simulating the role of a **Data Analyst** at **VentureInsight**, a leading research firm providing data-driven insights to venture capital firms and startup investors.

## 📊 Project Overview

As a new Data Analyst at VentureInsight, your mission is to explore and analyze a comprehensive venture capital database containing information about **startups**, **venture funds**, **acquisitions**, **investments**, and **key people** in the startup ecosystem.  
The goal is to deliver actionable insights that help clients make smarter, data-backed investment decisions.

### 🧩 Database Structure

The database consists of the following key tables:

| Table | Description |
|--------|-------------|
| **company** | Information about startups (funding, status, category) |
| **fund** | Details about venture capital funds |
| **funding_round** | Data on investment rounds |
| **investment** | Records of specific investments |
| **acquisition** | Information about company acquisitions |
| **people** | Details about founders, employees, and investors |
| **education** | Educational backgrounds of individuals |

An ER diagram illustrates the relationships among these tables.

---

## 🔍 Analytical Tasks

This project is divided into **10 core analyses**, each addressing a unique business question relevant to venture capital decision-making.

### 1. Startup Landscape Analysis
Determine the overall startup success rate by calculating how many companies have **closed**, are **operating**, or have been **acquired**.

### 2. Sector Analysis for US Investors
Identify **news and media startups** in the **USA** and calculate their **total historical funding**, sorted by funding totals in descending order.

### 3. Analyzing Cash Acquisitions
Quantify the **total value of cash-based acquisitions** between **2011–2013**, highlighting post-recession acquisition trends.

### 4. Identifying Industry Influencers
List individuals whose **Twitter usernames start with “Silver”** — potential industry influencers for marketing outreach.

### 5. Finding Finance Influencers
Find finance-focused influencers with **“money”** in their Twitter handles and **last names starting with “K”**.

### 6. Geographic Investment Analysis
Aggregate and compare **total venture funding by country**, ranking nations by total investment raised.

### 7. Funding Round Volatility Analysis
Analyze **funding round volatility** by identifying dates with the largest disparities between **minimum and maximum funding amounts**, excluding zero values.

### 8. Fund Activity Classification
Categorize venture funds by investment activity level:

- `high_activity` — 100+ investments  
- `middle_activity` — 20–99 investments  
- `low_activity` — fewer than 20 investments

### 9. Investment Strategy by Fund Activity
Compare **average funding rounds per company** across fund activity categories to reveal differences in investment strategies.

### 10. Employee Education Impact on Startup Success
Investigate whether **employee education levels** influence **startup success** by comparing education data between **failed** and **successful** companies.

---

## 🧠 Key Skills Demonstrated

- **SQL / Data Querying**
- **Data Cleaning and Joins**
- **Exploratory Data Analysis (EDA)**
- **Business Intelligence Reporting**
- **Data Visualization (optional extension)**
- **Analytical Storytelling**

---

## 🛠️ Tools & Technologies

- **SQL** (PostgreSQL / MySQL)
- **BI Tools**: Power BI / Tableau (optional visualization)
- **Python / Pandas** (for extended analysis)
- **Excel** (for result validation or summaries)

---

## 📈 Insights & Takeaways

Through these analyses, you will:

- Understand patterns in startup survival and investment success  
- Identify key funding trends across sectors and geographies  
- Explore the relationship between fund activity and investment strategies  
- Discover how human capital (education) may correlate with startup outcomes  

---

## 📂 Project Files

| File | Description |
|------|-------------|
| `Venture Insights.pdf` | Full project task brief and business questions |
| `queries.sql` | SQL scripts for each analysis task |
| `venture_insights_report.ipynb` | (Optional) Python notebook for analysis and visualization |
| `README.md` | Project documentation (this file) |

---

## 💡 Future Improvements

- Automate report generation using **Python dashboards** or **Power BI pipelines**  
- Incorporate **real-time VC and startup datasets**  
- Add **predictive analytics** for startup success modeling  

---

## 🏁 Conclusion

This project simulates real-world data analysis for venture capital decision-making — transforming raw relational data into actionable insights that drive **investment strategy**, **market understanding**, and **performance evaluation**.

---

**Author:** Jeffrey Hullinger  
**Role:** Data Analyst  
**Project:** Venture Insights — BI Analytics Portfolio Project  
**Date:** 2025  

---

