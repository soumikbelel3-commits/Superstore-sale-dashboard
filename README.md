# 🛒 Superstore Sales Analytics — End-to-End Data Analyst Project


> **Industry:** Retail &nbsp;|&nbsp; **Domain:** Sales Analytics &nbsp;|&nbsp; **Period:** 2015–2018 &nbsp;|&nbsp; **Records:** 9,800 &nbsp;|&nbsp; **Revenue Analysed:** $2.26M

---

## 📌 Project Overview

A full end-to-end Data Analyst project built on the **Global Superstore** dataset. This project covers every stage of the analytics lifecycle — from raw data ingestion and cleaning to SQL querying, statistical analysis, EDA visualisations, Power BI dashboard design, and boardroom-ready strategic recommendations.

The analysis uncovers **$460,000/year in actionable revenue opportunities** and identifies key profit leakage points across product categories and US regions.

---

## 🗂️ Table of Contents

- [Business Scenario](#-business-scenario)
- [Dataset](#-dataset)
- [Project Structure](#-project-structure)
- [Tech Stack](#-tech-stack)
- [Key Findings](#-key-findings)
- [Steps Covered](#-steps-covered)
- [Visualisations](#-visualisations)
- [SQL Queries](#-sql-queries)
- [Power BI Dashboard](#-power-bi-dashboard)
- [Strategic Recommendations](#-strategic-recommendations)
- [How to Run](#-how-to-run)
- [Resume Bullets](#-resume-bullets)

---

## 🏢 Business Scenario

**GlobalMart Inc.** is a US-based retail chain selling across three product categories — Furniture, Office Supplies, and Technology — to Consumer, Corporate, and Home Office customer segments across four US regions.

**Objective:** Identify revenue drivers, underperforming segments, and profit leakage points to drive a 15%+ profitability improvement in FY2019.

**Stakeholders:** VP Sales, CFO, Head of Supply Chain, Marketing Director, Product Management

---

## 📊 Dataset

| Property | Detail |
|---|---|
| Source | Global Superstore (Kaggle) |
| File | `train.csv` |
| Rows | 9,800 |
| Columns | 18 |
| Date Range | January 2015 – December 2018 |
| Geography | United States (4 Regions, 49 States) |

**Key columns:** `Order ID`, `Order Date`, `Ship Date`, `Ship Mode`, `Customer ID`, `Segment`, `Region`, `Category`, `Sub-Category`, `Sales`

---

## 📁 Project Structure

```
superstore-sales-analytics/
│
├── data/
│   └── train.csv                   # Raw dataset
│
├── notebooks/
│   └── superstore_eda.ipynb        # Full EDA notebook
│
├── sql/
│   └── business_queries.sql        # 10 production SQL queries
│
├── visuals/
│   ├── chart1_monthly_trend.png
│   ├── chart2_category_rev.png
│   ├── chart3_region.png
│   ├── chart4_segment.png
│   ├── chart5_subcategory.png
│   ├── chart6_yearly_growth.png
│   └── chart7_heatmap.png
│
├── report/
│   └── superstore_da_project.docx  # Full professional report (11 steps)
│
├── requirements.txt
└── README.md
```

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| **Python 3.10+** | Data cleaning, EDA, feature engineering |
| **Pandas & NumPy** | Data manipulation and transformation |
| **Matplotlib & Seaborn** | Statistical visualisations |
| **MySQL / SQL** | Business queries, window functions, CTAs |
| **Power BI** | Interactive dashboard design |
| **DAX** | Calculated measures and KPIs |

---

## 💡 Key Findings

| Finding | Impact |
|---|---|
| 📈 **20.3% YoY Revenue Growth** (2017→2018) | Business momentum is accelerating |
| 💻 **Technology = 18% margin** vs Furniture = 6% | Furniture is the biggest profit drag |
| 🌍 **West region outperforms all others** | Central region significantly underperforms |
| 🏢 **Top 20% customers = ~80% of revenue** | Classic Pareto — CLV management critical |
| 📦 **123 bulk-order outlier transactions** | Untapped corporate account opportunity |
| 📅 **Q4 is the strongest revenue quarter** | Seasonal campaign timing opportunity |

---

## 📋 Steps Covered

| Step | Topic |
|---|---|
| 1 | Business Understanding — scenario, stakeholders, financial context |
| 2 | Dataset Overview — column dictionary, KPI identification |
| 3 | Business Questions — 15 descriptive, diagnostic, and predictive questions |
| 4 | Data Cleaning — missing values, type fixing, feature engineering, outlier detection |
| 5 | EDA — 7 visualisations with business narrative |
| 6 | SQL Analysis — 10 queries with CTEs, window functions, running totals |
| 7 | Statistical Insights — CV, Pareto, hypothesis testing, seasonality |
| 8 | Power BI Design — 3-page dashboard, 8 DAX measures, calculated columns |
| 9 | Business Insights — what's working, failing, and leaking |
| 10 | Strategic Recommendations — short/medium-term actions, $460K impact estimate |
| 11 | Resume Bullet Points — 6 ATS-optimised bullets |

---

## 📈 Visualisations

| Chart | Insight |
|---|---|
| Monthly Revenue Trend | Clear Q4 seasonality; consistent YoY growth |
| Revenue by Category | Technology leads; Furniture high revenue, low margin |
| Region Performance | West dominates; Central significantly underperforms |
| Customer Segment Share | Consumers 51%, Corporate 30%, Home Office 19% |
| Top 10 Sub-Categories | Phones and Chairs are top revenue drivers |
| Annual YoY Growth | Acceleration to 20.3% in 2018 |
| Category × Region Heatmap | Technology concentrated in West/East |

---

## 🗃️ SQL Queries

Ten production-grade queries covering:

- ✅ Annual revenue summary with AOV (`GROUP BY`, `COUNT DISTINCT`)
- ✅ Category profit analysis (inline `CASE` margin logic)
- ✅ Regional ranking (`DENSE_RANK`, `OVER`)
- ✅ Top 10 customers by CLV (`CTE` + window function)
- ✅ Month-over-month growth (`LAG`)
- ✅ Cumulative running total (`ROWS BETWEEN UNBOUNDED PRECEDING`)
- ✅ Category × Region matrix (`RANK PARTITION BY`)
- ✅ Customer Lifetime Value with tenure (`DATEDIFF`, `MIN/MAX`)
- ✅ YoY regional growth (`LEAD/LAG PARTITION BY Region`)
- ✅ Shipping mode performance analysis

---

## 📊 Power BI Dashboard

**3-page dashboard design:**

**Page 1 — Executive Summary**
- KPI cards: Revenue, Orders, Customers, AOV, YoY Growth %
- Monthly trend line chart
- Top 5 customers bar chart
- Revenue by category donut

**Page 2 — Sales & Operations**
- US filled map (state-level revenue)
- Sub-category revenue with margin overlay
- Category × Region matrix (conditional formatting)
- Slicers: Year, Region, Category, Segment

**Page 3 — Customer Intelligence**
- Segment revenue by year (stacked bar)
- Repeat vs new customers
- Top 20 CLV customer table
- New vs returning customer trend

**Key DAX Measures:**
```dax
Total Revenue    = SUM(superstore[Sales])
Total Orders     = DISTINCTCOUNT(superstore[Order ID])
AOV              = DIVIDE([Total Revenue], [Total Orders])
YoY Growth %     = DIVIDE([CY Rev] - [PY Rev], [PY Rev])
Est Profit       = SUMX(superstore, superstore[Sales] * [Margin Rate])
Repeat Customers = CALCULATE(DISTINCTCOUNT([Customer ID]), [Order Count] >= 2)
```

---

## ⚙️ How to Run

**1. Clone the repository**
```bash
git clone https://github.com/yourusername/superstore-sales-analytics.git
cd superstore-sales-analytics
```

**2. Install dependencies**
```bash
pip install -r requirements.txt
```

**3. Run the EDA notebook**
```bash
jupyter notebook notebooks/superstore_eda.ipynb
```

**4. Run SQL queries**
```bash
# Import train.csv into MySQL as 'superstore' table, then:
mysql -u root -p your_db < sql/business_queries.sql
```

**`requirements.txt`**
```
pandas>=1.5.0
numpy>=1.23.0
matplotlib>=3.6.0
seaborn>=0.12.0
jupyter>=1.0.0
```

---

## 🎯 Strategic Recommendations

| Initiative | Est. Revenue Impact | Timeframe |
|---|---|---|
| Corporate Loyalty Program (top 100 CLV customers) | +$120,000/yr | 0–3 months |
| Central Region Sales Coverage Fix | +$80,000/yr | 0–3 months |
| Furniture Margin Audit (Tables/Bookcases) | +$30,000 profit | 0–3 months |
| Technology Category Expansion | +$180,000/yr | 3–12 months |
| Q4 Campaign Optimisation | +$50,000/yr | 3–6 months |
| **Total Estimated Impact** | **+$460,000/yr** | |

---

## 📝 Resume Bullets

> Copy-paste ready for your CV or LinkedIn

- Conducted end-to-end sales analysis on 9,800 retail transactions ($2.26M revenue) using Python (Pandas, Seaborn, Matplotlib), uncovering 20.3% YoY growth opportunity and $44K in annual Furniture margin leakage
- Engineered 6 new analytical features including estimated profit, ship days, and outlier flags; identified 123 high-value bulk-order transactions representing untapped corporate account management revenue
- Wrote 10 production-grade SQL queries using CTEs, window functions (LAG, LEAD, RANK, DENSE_RANK), and running totals to answer stakeholder questions on CLV, regional growth, and shipping performance
- Designed a 3-page Power BI dashboard with 8 custom DAX measures enabling C-level executives to monitor KPIs and drill down by region, category, and customer segment
- Delivered 5 strategic recommendations with estimated $460,000/yr financial impact, including a Corporate Loyalty Program and Central Region sales coverage intervention
- Applied statistical analysis (CV, Pareto 80/20, hypothesis testing) to validate business assumptions and provide confidence-weighted investment recommendations to senior leadership

---

## 📬 Contact

**Author:** [Your Name]  
**LinkedIn:** [linkedin.com/in/yourprofile](https://linkedin.com/in/yourprofile)  
**Email:** your.email@example.com

---

*⭐ If you found this project useful, please star the repository!*
