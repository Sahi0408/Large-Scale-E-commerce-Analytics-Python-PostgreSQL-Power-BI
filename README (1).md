<div align="center">

# 🛒 Large-Scale E-Commerce Analytics

### End-to-End Data Analytics Solution — Python · PostgreSQL · Power BI



</div>

---

## 📌 Project Overview

This project delivers a **complete data analytics pipeline** for a large-scale e-commerce dataset — from raw transactional data to interactive business dashboards. By combining Python for data processing, PostgreSQL for business queries, and Power BI for visualization, it transforms millions of records into actionable insights on customer behavior, product performance, revenue trends, and market segmentation.

---

## 🎯 Objectives

| # | Goal |
|---|------|
| 1 | Analyze customer purchasing patterns and segment high-value customers |
| 2 | Identify top-performing products by revenue and quantity |
| 3 | Evaluate revenue trends across time (hourly, daily, monthly) |
| 4 | Discover geographic sales distribution by country |
| 5 | Build interactive Power BI dashboards for business stakeholders |

---

## 🛠️ Tech Stack

| Layer | Tools |
|-------|-------|
| **Language** | Python 3.10+ |
| **Data Processing** | Pandas, NumPy |
| **Visualization** | Matplotlib, Power BI |
| **Database** | PostgreSQL |
| **Version Control** | Git & GitHub |

---

## 📂 Project Structure

```
Large-Scale-Ecommerce-Analytics/
│       
│
├── 📁 notebooks/
│   └── ecommerce_data_cleaning.ipynb
│  
│   
│
├── 📁 sql/
│   └── ecommerce_queries.sql  # All SQL business analysis queries
│
├── 📁 dashboard/
│   └── ecommerce_dashboard.pbix  # Power BI dashboard file
│
├
└── README.md
```

---

## 🔧 Data Cleaning & Feature Engineering

The raw dataset was processed through the following steps:

- ✅ **Missing value handling** — imputed or dropped based on column significance
- ✅ **Duplicate removal** — eliminated redundant transaction records
- ✅ **Revenue column** — derived as `Quantity × Unit Price`
- ✅ **Datetime features** — extracted `Year`, `Month`, `Month_Name`, `Day_Name`, `Hour`
- ✅ **Format standardization** — normalized column types for SQL and BI compatibility

---

## 📊 Exploratory Data Analysis (EDA)

Comprehensive EDA was performed across multiple dimensions:

- 📅 **Monthly Revenue Trends** — seasonal patterns and growth curves
- 🌍 **Revenue by Country** — geographic performance breakdown
- ⏰ **Revenue by Hour** — peak shopping time analysis
- 📆 **Revenue by Day of Week** — weekday vs. weekend behavior
- 🏆 **Top Products by Revenue** — high-grossing SKUs
- 📦 **Top Products by Quantity** — most frequently purchased items
- 👤 **Customer Purchasing Behavior** — frequency, recency, and spend analysis

---

## 🗄️ SQL Business Analysis

Key business questions answered through structured SQL queries:

```sql
-- Sample: Top 10 Customers by Revenue
SELECT CustomerID,
       ROUND(SUM(Revenue)::numeric, 2) AS total_revenue
FROM transactions
GROUP BY CustomerID
ORDER BY total_revenue DESC
LIMIT 10;
```

| Query | Description |
|-------|-------------|
| Total Revenue | Aggregate revenue across all transactions |
| Total Orders | Count of unique order IDs |
| Total Customers | Count of unique customer IDs |
| Average Order Value | Mean revenue per order |
| Top Products by Revenue | Highest-grossing products |
| Top Products by Quantity | Best-selling products by units |
| Top Customers by Revenue | High-value customer identification |
| Revenue by Country | Country-wise sales breakdown |
| Monthly Revenue Trends | Month-over-month performance |
| Revenue by Hour | Intraday demand patterns |

> 📄 Full SQL scripts are available in the [`/sql`](./sql/) directory.

---

## 📊 Power BI Dashboards

The project includes **4 interactive dashboards**, each targeting a specific analytical perspective.

### 1️⃣ Executive Summary
> High-level KPIs for leadership decision-making

- Total Revenue · Total Orders · Total Customers · Average Order Value
- Monthly Revenue Trend (line chart)
- Revenue by Country (map / bar)

### 2️⃣ Product Analysis
> Deep dive into product-level performance

- Top 10 Products by Revenue
- Top 10 Products by Quantity Sold
- Products with Highest Average Price

### 3️⃣ Customer Analysis
> Understanding who your customers are

- Top Customers by Revenue
- Top Customers by Order Frequency
- Customer Revenue Distribution by Country

### 4️⃣ Time Analysis
> When do customers buy?

- Monthly Revenue Trend
- Revenue by Day of Week
- Revenue by Hour of Day

---

## 💡 Key Business Insights

> 📌 The following insights were derived from the analysis:

1. **Revenue concentration** — A small group of customers drove a disproportionately large share of total revenue, suggesting high ROI on loyalty and retention programs.
2. **Product performance** — A handful of products consistently led both in revenue and quantity, making them critical to inventory and marketing strategy.
3. **Geographic variance** — Sales performance varied significantly across countries, highlighting opportunities for targeted regional campaigns.
4. **Peak demand windows** — Revenue spiked during specific hours and days, enabling more effective scheduling of promotions and flash sales.
5. **Seasonality** — Clear monthly patterns indicate seasonal demand cycles that can be used for proactive planning.

---

## ⚙️ Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/Large-Scale-Ecommerce-Analytics.git
cd Large-Scale-Ecommerce-Analytics
```

### 2. Install Python Dependencies
```bash
pip install -r requirements.txt
```

### 3. Set Up PostgreSQL
```bash
# Create database and run schema/data scripts
psql -U postgres -c "CREATE DATABASE ecommerce;"
psql -U postgres -d ecommerce -f sql/business_queries.sql
```

### 4. Run the Notebooks
Open Jupyter and run the notebooks in order:
```bash
jupyter notebook notebooks/
```

### 5. Explore the Dashboard
Open `dashboard/ecommerce_dashboard.pbix` in **Power BI Desktop**.

---

## 📦 Requirements

```
pandas>=2.0
numpy>=1.24
matplotlib>=3.7
sqlalchemy>=2.0
psycopg2-binary>=2.9
jupyter>=1.0
```

> Install all at once: `pip install -r requirements.txt`

---

## 🚀 Project Outcome

Built an **end-to-end data analytics solution** that:

- Cleaned and engineered features from raw e-commerce transaction data
- Answered 10+ critical business questions using SQL
- Delivered 4 interactive Power BI dashboards for business stakeholders
- Surfaced actionable insights on customers, products, time, and geography

---

## 📬 Contact

**Your Name**  
  Sahil

---

<div align="center">
  <sub>⭐ If you found this project helpful, please give it a star!</sub>
</div>
