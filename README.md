Sales Trend Analysis Using SQL Aggregations
This project analyzes monthly sales trends using a simulated e-commerce dataset.
The main goal is to understand how revenue and order volume change over time using SQL-style aggregation techniques.

Objective
To extract insights from online sales data by calculating monthly revenue and order volume for the year 2022.

Tools Used
PostgreSQL / MySQL / SQLite (for SQL query structure)

Python (Pandas, Matplotlib, Seaborn)

Simulated dataset: online_sales.orders

Dataset Fields
order_id

order_date

amount

product_id

The dataset contains order-level data for the year 2022.

What the SQL Does
sql
Copy
Edit
SELECT
  EXTRACT(YEAR FROM order_date) AS year,
  EXTRACT(MONTH FROM order_date) AS month,
  COUNT(DISTINCT order_id) AS order_volume,
  SUM(amount) AS total_revenue
FROM online_sales.orders
WHERE order_date BETWEEN '2022-01-01' AND '2022-12-31'
GROUP BY year, month
ORDER BY year, month;
Output
The result is:

A table showing monthly revenue and number of unique orders

A visualization chart that makes it easy to spot trends over the year

Deliverables
SQL Script (sales_trend_analysis.sql)

Dataset (online_sales_orders.csv)

Results Table (monthly_sales_summary.csv)

Trend Chart (monthly_sales_trend.png)

Final Report (Sales_Trend_Analysis_Report_Humanized.pdf)

Conclusion
This project demonstrates how simple SQL aggregation functions can be used to extract meaningful business insights from transactional data.

