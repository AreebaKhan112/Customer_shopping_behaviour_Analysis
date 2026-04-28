# Customer Shopping Behavior Analysis

An end-to-end data analytics project analyzing retail customer shopping behavior to identify the key factors driving revenue and sales. Built using Python, SQL, and Power BI.

---

## Project Overview

This project simulates a real-world data analytics workflow for a retail business. The objective was to clean and analyze a customer shopping dataset to determine which demographic factors — specifically gender, subscription status, and age group — have the greatest influence on revenue generation.

The insights from this analysis are intended to help the business make more informed decisions around marketing, customer retention, and product strategy.

---

## Business Problem

The business wanted to understand:

- Which customer demographic generates the most revenue and displays the strongest loyalty?
- Does having a subscription influence how much a customer spends?
- Which products rely on discounts to sell, and when should they be stocked up?
- How can the business better target its largest customer segment (young adults)?

---

## Dataset

- **Source:** Open-source dataset from a public GitHub repository
- **Size:** 3,900 rows × 18 columns
- **Data Types:** Mix of numeric and categorical (text) values

**Key columns include:**

| Column | Description |
|---|---|
| Age | Customer age |
| Gender | Male / Female |
| Item Purchased | Name of the product |
| Category | Product category (e.g., Clothing, Footwear) |
| Purchase Amount (USD) | Transaction value |
| Subscription Status | Whether the customer has a subscription |
| Review Rating | Customer satisfaction score (1–5) |
| Frequency of Purchases | How often the customer shops |
| Previous Purchases | Number of prior transactions |
| Discount Applied | Whether a discount was used |

---

## Tools & Technologies

| Tool | Purpose |
|---|---|
| Python (pandas) | Data cleaning and transformation |
| Jupyter Notebook | Development environment |
| SQL | Business analysis and querying |
| Power BI | Dashboard and data visualization |

---

## Project Workflow

### 1. Data Loading & Exploration
The raw CSV dataset was loaded into a Jupyter Notebook using pandas. Initial exploration was performed to understand the structure of the data, check for missing values, and review data types across all columns.

### 2. Data Cleaning & Transformation
The following steps were applied to prepare the data for analysis:

- **Null value treatment:** Missing values in the `Review_Rating` column were filled using the median rating per product category. The median was chosen over the mean due to its robustness against outliers.
- **Column name standardization:** Spaces in column names were replaced with underscores for consistency and SQL compatibility.
- **Age group segmentation:** Customers were grouped into four age categories based on the age ranges in the dataset to enable demographic-level analysis.
- **Frequency encoding:** The `Frequency_of_Purchases` column (text values) was mapped to numeric equivalents and stored in a new column for quantitative use.
- **Column cleanup:** Duplicate and redundant columns were identified and removed.

### 3. SQL Analysis
The cleaned dataset was loaded into a SQL database. Ten queries were written to answer specific business questions covering:

- Revenue breakdown by gender
- Average spend by subscription status
- Age group distribution across the customer base
- Repeat purchase behavior
- Discount dependency by product category

### 4. Power BI Dashboard
The SQL database was connected to Power BI, where an interactive dashboard was built to visualize the key findings. The dashboard allows users to explore data across dimensions including gender, subscription status, age group, and product category.

---

## Key Findings

- **Male customers generate more total revenue** than female customers, reflecting the current composition of the customer base rather than differences in individual spending.
- **Subscribed and non-subscribed customers spend similar amounts on average**, suggesting the subscription plan does not provide sufficient financial incentive to meaningfully change spending behavior.
- **Non-subscribed customers generate more overall revenue** and make up the majority of repeat buyers, indicating the subscription program is underperforming in terms of attracting and retaining customers.
- **The customer base is largely loyal**, with a strong proportion of repeat buyers across the dataset.
- **Hats, sweaters, coats, sneakers, and pants are heavily discount-dependent**, meaning they rarely sell at full price without a promotion.
- **Young adults make up the largest customer segment** in the dataset.

---

## Business Recommendations

**1. Invest in women's clothing and marketing**
While male customers currently generate more revenue, women's clothing represents a significantly larger market opportunity. Expanding the women's product range and improving female-targeted marketing has strong potential to grow the customer base and increase long-term revenue.

**2. Revamp the subscription package**
The similarity in spend between subscribed and non-subscribed customers, combined with non-subscribers dominating repeat purchases, indicates the current subscription offering is not compelling enough. Adding more meaningful benefits — such as deeper discounts or exclusive perks — could improve subscription uptake and customer retention.

**3. Stock discount-reliant products ahead of sale periods**
Products like hats, sweaters, coats, sneakers, and pants rely on discounts to sell. Increasing supply of these items ahead of key sales events (e.g., Christmas, seasonal clearances) would allow the business to move more inventory during periods when promotional pricing is already in place.

**4. Align product catalog with youth fashion trends**
With young adults as the dominant customer segment, keeping the product catalog current with trending styles is important for maintaining engagement and reducing reliance on discounts to drive conversions.

---
