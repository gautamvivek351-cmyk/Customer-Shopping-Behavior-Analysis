# Customer-Shopping-Behavior-Analysis
End-to-end Data Analytics project using Python, SQL, and Power BI to analyze 3,900+ customer transactions. Performed data cleaning, EDA, SQL-based business analysis, and built an interactive dashboard to uncover customer behavior, sales trends, and actionable business insights.

# 📊 Customer Shopping Behavior Analysis

An end-to-end data analytics project analyzing 3,900 retail transactions to uncover customer segments, revenue drivers, and purchasing patterns — built using **Python, SQL, and Power BI**.

## 📌 Business Problem

A leading retail company wants to better understand its customers' shopping behavior in order to improve sales, customer satisfaction, and long-term loyalty. Management had noticed shifts in purchasing patterns across demographics, product categories, and sales channels, and wanted to understand which factors — discounts, reviews, seasons, or payment preferences — actually drive consumer decisions and repeat purchases.

**Guiding business question:**
> How can the company leverage consumer shopping data to identify trends, improve customer engagement, and optimize marketing and product strategies?

## 🗂️ Repository Contents

| File | Description |
|---|---|
| `customer_shopping_data.csv` | Raw dataset — 3,900 rows, 18 columns |
| `Customer_Shopping_Behavior_Analysis.ipynb` | Python notebook: data loading, cleaning, feature engineering, and database loading |
| `customer_shopping_behaviour.sql` | 10 SQL queries answering key business questions |
| `customer_behavior_dashboard.pbix` | Interactive Power BI dashboard |

## 🧹 Data Preparation (Python)

- **Loaded** the dataset using `pandas` and explored structure with `.info()` and `.describe()`
- **Handled missing values**: imputed 37 missing `Review Rating` entries using the median rating per product category
- **Standardized columns** to snake_case for consistency
- **Engineered features**:
  - `age_group` — binned customer ages into Young Adult, Adult, Middle-aged, and Senior groups
  - `purchase_frequency_days` — mapped purchase frequency labels (e.g., "Weekly", "Quarterly") to numeric day intervals
- **Removed redundancy**: confirmed `discount_applied` and `promo_code_used` were identical across all rows and dropped the duplicate column
- **Loaded the cleaned dataset into a SQL database** using SQLAlchemy for downstream SQL analysis

## 🧮 Business Analysis (SQL)

Ten queries were written to answer specific business questions, including:

1. Revenue comparison by gender
2. High-spending customers who still used discounts
3. Top 5 products by average review rating
4. Purchase amount comparison: Standard vs. Express shipping
5. Subscriber vs. non-subscriber spending behavior
6. Top 5 products most dependent on discounts
7. Customer segmentation into New / Returning / Loyal tiers
8. Top 3 best-selling products per category
9. Relationship between repeat purchases and subscription status
10. Revenue contribution by age group

## 📈 Key Insights

- **Male customers generated ~2.1x more revenue** than female customers ($157,890 vs. $75,191)
- **80% of customers fall into the "Loyal" segment** (3,116 of 3,900), with far fewer New (83) or Returning (701) customers
- **Discount dependency is highest on Hats, Sneakers, and Coats**, each with a discount rate near 50%
- **Express shipping customers spend marginally more** on average ($60.48) than Standard shipping customers ($58.46)
- **Non-subscribers generate significantly more total revenue** ($170,436) than subscribers ($62,645), despite similar average spend per customer — driven by a much larger non-subscriber base
- **Revenue is fairly evenly spread across age groups**, with Young Adults contributing marginally the most ($62,143)

## 📊 Dashboard (Power BI)

An interactive dashboard was built featuring:
- KPI cards for total customers, average purchase amount, and average review rating
- Slicers for subscription status, gender, category, and shipping type
- Revenue and sales breakdowns by category and age group
- A donut chart visualizing subscriber vs. non-subscriber split

## 💡 Business Recommendations

- **Boost subscriptions** by promoting exclusive subscriber benefits, given the current revenue gap favoring non-subscribers
- **Launch loyalty programs** to convert Returning customers into the high-value Loyal segment
- **Review discount policy** on high-dependency items (Hats, Sneakers, Coats) to protect margins
- **Highlight top-rated, best-selling products** (Gloves, Sandals, Boots) in marketing campaigns
- **Target high-revenue segments** — Young Adults and Express-shipping users — in future marketing spend

## 🛠️ Tools Used

- **Python** (pandas, SQLAlchemy) — data cleaning and feature engineering
- **SQL** — structured business-question analysis
- **Power BI** — interactive dashboarding and visualization


## 📄 License

This project is licensed under the MIT License — see `LICENSE` for details.
