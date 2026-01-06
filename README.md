# 🛒 Instacart Market Basket: Data Integrity & Consumer Behavior Analysis

## 🎯 Project Overview
This project focuses on a comprehensive **Data Wrangling** and **Exploratory Data Analysis (EDA)** process for a modified Instacart dataset. The primary goal was to transform raw, fragmented grocery data into a high-fidelity dataset to uncover meaningful patterns in customer shopping habits, order frequency, and product loyalty.

## 🛠️ Data Engineering & Cleaning Pipeline
Managing five relational tables (`orders`, `products`, `order_products`, `aisles`, and `departments`) required a systematic approach to ensure data consistency across the entire schema.



### Key Data Integrity Steps:
* **Schema Normalization:** Identified and corrected inconsistent data types, ensuring columns like `order_hour_of_day` and `order_dow` (day of week) were within logical bounds.
* **Missing Value Imputation:** * `days_since_prior_order`: Handled `NaN` values (representing first-time customers) by imputing `0.0` to maintain numerical consistency.
    * `product_name`: Standardized missing entries as `'unknown'` to preserve categorical integrity.
    * `add_to_cart_order`: Resolved missing values with a placeholder (`999`) to facilitate integer conversion.
* **Deduplication:** Performed multi-stage duplicate checks on unique identifiers and cross-table references to eliminate redundant noise.

## 📊 Exploratory Data Analysis (EDA)
With the cleaned data, I analyzed the temporal distribution of orders and customer retention metrics:

### 1. Temporal Shopping Patterns
Using **Matplotlib** and **Seaborn**, I visualized when customers are most active:
* **Peak Hours:** Identification of high-traffic windows for grocery deliveries.
* **Weekly Trends:** Analysis of weekend vs. weekday demand.



### 2. Retention & Loyalty Metrics
* **Reorder Rate Analysis:** Calculated the proportion of repeat purchases to measure brand loyalty and product stickiness.
* **Order Frequency:** Analyzed the distribution of days between orders to understand the typical customer lifecycle.

## 🛠️ Tech Stack
* **Language:** Python 3.12.x
* **Data Manipulation:** Pandas, NumPy.
* **Visualization:** Matplotlib, Seaborn.
* **Methods:** `merge()`, `fillna()`, `value_counts()`, `duplicated()`, `astype()`.

## 📈 Key Business Insights
* **Operational Optimization:** Order peaks occur during morning hours and weekends, suggesting critical windows for staffing and logistics optimization.
* **Customer Loyalty:** A high reorder rate in specific departments (e.g., Produce) indicates strong customer retention and reliance on the platform for daily essentials.
* **Actionable Data:** The refined dataset is now prepared for advanced Machine Learning tasks, such as Market Basket Analysis or Recommender Systems.
