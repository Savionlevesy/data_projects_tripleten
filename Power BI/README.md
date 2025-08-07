# 🛍️ Shopify App Landscape Analysis — Sprint 6

## 📊 Overview

This Power BI project analyzes publicly available data from the Shopify App Store. The goal is to understand what factors contribute to a successful Shopify app. This analysis was conducted as part of the TripleTen Business Intelligence Analyst program, Sprint 6.

## 🧠 Project Objective

Identify patterns and relationships between app metadata, reviews, and developer behavior to determine what drives app success on the Shopify marketplace.

Key research questions:
- How many apps are active on the Shopify App Store?
- How does review volume and sentiment evolve over time?
- Do developer responses impact user ratings?
- Which developers consistently earn high ratings or feedback?

---

## 📂 Data Sources

- **apps.xlsx**: Contains app metadata (ID, name, developer, etc.)
- **categories.xlsx**: App classification data
- **apps_categories.xlsx**: Join table between apps and categories
- **reviews.xlsx**: User reviews, ratings, helpfulness votes, developer replies

---

## 📁 Report Pages & Visualizations

### 📌 Part 1: App Landscape
📍**Power BI Sheet Name**: `App Landscape`
- ✅ **KPI Card** — Total unique number of apps
- 📈 **Line Chart** — Review volume over time using `lastmod` (not in date hierarchy)
- 📉 **Scatterplot** — `reviews_count` vs. average `rating`  
  - 📝 Annotated with interpretation in a text box

---

### 🗣️ Part 2: Reviews
📍**Power BI Sheet Name**: `Reviews`
- 🧮 **Calculated Column**: `helpful_reviews = rating * (1 + helpful_count)`
  - 📊 KPI Card showing average `helpful_reviews`
- 🧠 **Calculated Column**: `developer_answered = IF(ISBLANK(developer_reply), 0, 1)`
  - 📉 Scatterplot: Average `rating` by `developer_answered`

---

### 💬 Part 3: App Reviews
📍**Power BI Sheet Name**: `App Reviews`
- 🔗 **Relationships Created**:
  - `Reviews[app_id]` → `Apps[id]` (Many-to-One)
- 📊 **Bar Chart**: `developer` vs. sum of `rating`
- 🧮 **Bar Chart (cleaned)**: `developer` vs. average `helpful_reviews`
- 💡 **Developer Responsiveness**:  
  - `developer` vs. average `developer_answered`  
  - Filter applied: `reviews_count > 500`

---

## 💡 Key Insights

- Many apps generate high review counts around update events (`lastmod`).
- A small number of developers receive both the most feedback and the highest `helpful_reviews` scores.
- Developer responsiveness (`developer_answered`) strongly correlates with better user ratings.
- Filtering out apps with low review counts revealed clearer trends in quality and support levels.

---

## 🛠️ Tools Used

- Power BI (Modeling, DAX, Visualizations)
- Excel (Initial data exploration)
- DAX Expressions for calculated fields and filters

---

## ✅ Skills Demonstrated

- Data modeling and relationship setup
- KPI tracking and time-series analysis
- DAX column creation (`IF`, `ISBLANK`, calculated fields)
- Insight-driven dashboard storytelling
- Responsive developer performance metrics

---

## 📁 File Included

- `Sprint 6 power BI savion levesy.pbix` — Full Power BI report file
- Screenshots documenting each visualization step (to be uploaded in GitHub repo)

---

## 👨‍💻 Author

**Savion Levesy**  
Business Intelligence Analyst | TripleTen Graduate  
📧 [Your Email]  
🌐 [GitHub Profile]

---

