📊 Superstore Sales Analysis – End-to-End Data Analytics Project

Replace with actual dashboard screenshot

📋 Project Overview
This comprehensive data analytics project analyzes 4 years of sales data (2015–2018) for a national retail chain operating across the United States. The dataset contains over 9,900 transactions, $2.3M in revenue, and spans three product categories: Furniture, Office Supplies, and Technology. The goal was to uncover growth opportunities, optimize profitability, and provide strategic recommendations to increase revenue by 15% while maintaining healthy margins.

The project follows a structured end-to-end analytics workflow:

1.Business Understanding

2.Data Cleaning & Feature Engineering (Python)

3.Exploratory Data Analysis (Python)

4.SQL Business Analysis

5.Statistical Insights

6.Power BI Dashboard Design

7.Strategic Recommendations

🎯 Business Problem
"Identify growth opportunities and profitability drivers across products, regions, and customer segments to increase revenue by 15% while maintaining 20% profit margins."

Stakeholders:

CEO, CFO, VP of Sales, Regional Sales Managers, Marketing Director, Supply Chain Manager

Financial Motivation:

$2.3M in sales with varying profitability

Regional disparities suggest untapped potential

Seasonal patterns can optimize inventory & marketing spend

Shipping efficiency impacts customer satisfaction and costs

📁 Dataset
The dataset is a CSV export from a retail superstore, containing 9,994 rows and 21 columns.

Column	Description
Row ID	Unique transaction ID
Order ID	Unique order identifier
Order Date	Date order placed
Ship Date	Date order shipped
Ship Mode	Shipping method (4 categories)
Customer ID	Unique customer ID
Customer Name	Customer full name
Segment	Customer segment (Consumer/Corporate/Home Office)
Country	All USA
City, State, Postal Code, Region	Geographic details
Product ID, Category, Sub-Category, Product Name	Product details
Sales	Transaction amount ($)
Key Metrics:

Total Revenue: $2,297,201

Total Orders: 5,009

Total Customers: 793

Avg Order Value: $458.66

Time Period: 2015–2018

🔍 Methodology
Step 1: Business Understanding
Defined industry (retail), stakeholders, business objectives, and financial importance.

Step 2: Data Cleaning & Feature Engineering (Python)
Handled missing postal codes (11 rows)

Removed duplicates

Converted date columns

Detected and capped outliers (top 1% of sales)

Engineered 15+ features:

Year, Month, Quarter, DayOfWeek

Shipping_Days, Is_Delayed

Order_Value, Items_Per_Order

Customer_Tenure_Days, Is_Repeat

Price_Tier (Low/Medium/High/Premium/Luxury)

Step 3: Exploratory Data Analysis (Python)
Univariate, bivariate, and time-series analysis

Correlation matrix

Key visualizations:

Sales distribution

Revenue by category, segment, region

Monthly/quarterly trends

Top states and products

Shipping mode analysis

Step 4: SQL Business Analysis
12 advanced SQL queries using:

Window functions (RANK, LAG, RUNNING TOTAL)

CTEs

RFM segmentation

YoY growth calculations

Customer lifetime value by segment

Step 5: Statistical Insights
Hypothesis testing (t-tests, ANOVA)

95% confidence intervals

Significant findings:

Corporate customers spend 22% more than Consumers (p < 0.001)

West region outperforms Central by 31% (p < 0.01)

Q4 sales are 45% higher than Q1 (p < 0.001)

Step 6: Power BI Dashboard Design
Three-page interactive dashboard:

Executive Summary – KPI cards, monthly trend, top products, revenue map

Sales Performance – region matrix, category breakdown, shipping analysis, slicers

Customer Insights – segmentation, repeat vs new, top customers, RFM scatter plot

DAX Measures: Total Revenue, Total Orders, Avg Order Value, YTD Growth, On-Time Delivery %, Customer Lifetime Value, Repeat Customer Rate, etc.

Step 7: Business Insights & Recommendations
Identified what's working (Technology, Corporate, West region, Q4)

Pinpointed money leaks (Central region, Tables/Bookcases, First Class delays)

Delivered short-term and long-term strategic actions with financial impact modeling

Estimated $1.2M cumulative revenue growth over 2 years at 335% ROI

💡 Key Insights
Area	Insight
Revenue Growth	34% growth from 2015 to 2018; Q4 contributes 35% of annual revenue
Product Performance	Technology leads with 36% of revenue; Phones, Chairs, Storage are top sub-categories
Customer Segments	Consumers (51% revenue), Corporate (30%), Home Office (19%) – Corporate has highest AOV
Geographic	West region dominates (32%); California alone = 20% of total sales
Shipping	Standard Class most popular (59%); avg delivery 4 days; First Class delays risk satisfaction
Repeat Customers	83% of revenue from repeat buyers – strong loyalty
Underperformers	Central region lags by 18% in AOV; Tables & Bookcases have low margins
📈 Strategic Recommendations
Short-Term (0–3 Months)
Fix First Class shipping delays – renegotiate carriers, adjust promised dates

Launch Central region intervention (dedicated manager, targeted campaign)

Implement Corporate loyalty program (tiered discounts, account managers)

Set minimum order value ($25) to reduce low-value transactions

Medium-Term (3–12 Months)
Home Office growth initiative (remote work bundles, influencer marketing)

Expand Technology category (accessories, bundles, seasonal promos)

Replicate West region best practices in Central/East

Optimize inventory (reduce slow-moving furniture, increase tech for Q4)

Financial Impact
Year 1: +$502K revenue

Year 2: +$706K revenue

Cumulative 2 years: +$1.208M

ROI: 335% (payback in 3.6 months)

🛠️ Technologies Used
Python (Pandas, NumPy, Matplotlib, Seaborn, SciPy) – data cleaning, EDA, statistics

SQL – advanced querying, window functions, CTEs

Power BI – interactive dashboards, DAX measures

Git / GitHub – version control and project sharing

