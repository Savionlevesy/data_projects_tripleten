# 🏙️ NYC Airbnb Data Analysis — TripleTen Project

## 📊 Project Overview

This project is part of the TripleTen Business Intelligence Analyst training program. It focuses on analyzing real-world Airbnb listing data in New York City to uncover actionable insights for improving listing performance, guest satisfaction, and booking strategy. The dataset includes listings, host information, pricing, reviews, availability, and more.

## 🔍 Business Objective

The main goal is to investigate how various factors—such as property type, price, location, host characteristics, and room availability—affect listing success and guest experience. Key stakeholders could use this analysis to:

- Optimize listing pricing for better revenue
- Identify high-performing neighborhoods
- Improve host response strategies
- Analyze review trends for customer satisfaction

## 📁 Dataset Description

### 🏘️ Listings Data
The `listings` dataset includes over 70 variables such as:
- `id`, `name`, `host_id`, `host_since`, `neighbourhood_group`, `room_type`
- `price`, `minimum_nights`, `number_of_reviews`, `reviews_per_month`
- `availability`, `host_response_rate`, `review_scores_*`, and many more

### 📅 Calendar Data
The `calendar` file records:
- Daily availability and pricing for each listing (`listing_id`, `date`, `available`, `price`, `minimum_nights`)

## 🧠 Key Questions Explored
- What neighborhoods have the highest average prices?
- Which room types are the most popular?
- Do superhosts earn better reviews?
- How does availability affect bookings?
- What price ranges receive the most reviews?

## 📈 Visualizations & Techniques

- **Bar Chart**: Average price by neighborhood group  
- **Line Chart**: Price trends over time  
- **Heatmap**: Room type density by borough  
- **Box Plot**: Review scores by property type  
- **Scatter Plot**: Price vs. number of reviews

## 🧹 Data Preparation

Steps performed:
- Cleaned null or invalid entries in pricing, availability, and reviews
- Converted text-based fields (e.g., `price`, `bathrooms_text`) into usable numerical values
- Extracted time-based metrics (e.g., `first_review`, `last_review`)
- Filtered extreme outliers (e.g., listings with very high nightly prices or invalid availability)

## ✅ Key Insights

- **Entire home/apt** listings are the most expensive but also the most reviewed.
- **Brooklyn and Manhattan** have the most listings and command higher nightly rates.
- Listings from **superhosts** have significantly better review scores.
- Price outliers above $800/night were often unavailable or unbooked.
- Reviews correlate with room type more than with price alone.

## 🛠 Tools Used

- **Python** (pandas, matplotlib, seaborn)
- **Tableau / Power BI** (for visualization)
- **Jupyter Notebook**
- **GitHub** (version control & documentation)

## 📄 File Structure

