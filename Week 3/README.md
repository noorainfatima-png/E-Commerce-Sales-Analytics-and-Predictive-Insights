# Week 3: Exploratory Data Analysis (EDA) & Customer Segmentation

## Overview

This phase focuses on uncovering actionable business insights from preprocessed e-commerce sales data. Through exploratory data analysis and customer segmentation modeling, this module identifies revenue drivers, customer purchasing patterns, and key behavioral segments to guide strategic decision-making.

---

## Objectives

* **Analyze Sales Performance:** Identify trends across time, geography, and product categories.
* **Customer Behavior Analysis:** Measure key metrics such as Average Order Value (AOV), purchase frequency, and customer lifetime value proxies.
* **RFM Segmentation:** Group customers using Recency, Frequency, and Monetary (RFM) analysis to optimize targeted marketing strategies.
* **Predictive Feature Preparation:** Engineer feature sets for subsequent machine learning models.

---

## Technical Stack & Libraries

* **Language:** Python 3.x
* **Data Manipulation:** `pandas`, `numpy`
* **Visualization:** `matplotlib`, `seaborn`, `plotly`
* **Clustering & Analytics:** `scikit-learn` (K-Means, StandardScaler)

---

## Project Structure

```text
Week 3/
├── data/
│   ├── processed_sales_data.csv    # Preprocessed dataset from Week 2
│   └── rfm_segments.csv            # Output dataset with RFM scores and clusters
├── notebooks/
│   ├── 01_eda_sales_trends.ipynb   # Exploratory visualization & trend analysis
│   └── 02_customer_rfm_segmentation.ipynb # RFM scoring and K-Means clustering
└── src/
    ├── visualization.py            # Helper scripts for plotting
    └── segmentation.py             # Feature scaling and clustering pipeline

```


## Key Insights & Findings

* **Top Revenue Drivers:** High-frequency buyers contribute to over 60% of total revenue.
* **Seasonality:** Peak sales volumes align with weekend promotions and end-of-quarter campaigns.
* **Customer Clusters:**
* **Champions:** High recency, high frequency, high spend.
* **At-Risk:** Low recency, high historical frequency and spend.
* **Recent Buyers:** High recency, low frequency.



