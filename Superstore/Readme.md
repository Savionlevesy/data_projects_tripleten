# 🛒 Superstore Returns Analysis Dashboard

## Overview
This project aims to identify the **root causes of returned orders** at the Superstore and provide actionable insights for the CEO to reduce return volumes. Using Tableau, we developed an interactive dashboard and supporting story to guide decision-making across geography, time, product category, and customer behavior.

---

## 📊 Project Summary

- **Objective**: Determine why customers are returning orders and how to reduce these returns.
- **Tools Used**: Tableau, Excel, PDF reports
- **Data Sources**:  
  - `Sample - Superstore - Orders.pdf`  
  - `Sample - Superstore - Returns.pdf`

---

## 🧠 Key Business Questions

1. What product categories and subcategories are returned most frequently?
2. Do sales correlate with returns by subcategory?
3. Which geographic areas (e.g., states, cities) have higher return rates?
4. Are certain customers more prone to returning items?
5. Is there a seasonal pattern to returns?
6. What is the financial impact of returns (e.g., lost revenue)?

---

## 📈 Visualizations

Each of the following worksheets supports one or more of the questions above:

- **Scatter Plot** – Total Sales vs. Total Returns by Product Subcategory
- **Bar Chart** – Return Rate by Product Category
- **Bar Chart** – Return Rate by Customer (filtered for customers with >1 order)
- **Map Visualization** – Return Rate by State
- **Line Chart** – Monthly Return Rate Trends
- **Composite Charts** – Blended metrics by Category & Region / Month & Segment

---

## 🧰 Data Preparation

- **Join**: Performed a LEFT JOIN of the Returns table onto the Orders table.
- **Calculated Field**:  
  ```tableau
  IF ISNULL([Returned]) THEN 0 ELSE 1 END
