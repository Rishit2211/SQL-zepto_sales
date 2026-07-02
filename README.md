# SQL Zepto Sales Analysis

## Overview

This project analyzes Zepto sales data using SQL to uncover business insights, customer purchasing behavior, product performance, and revenue trends. The analysis demonstrates the use of SQL queries for data cleaning, exploration, aggregation, and reporting.

## Objectives

* Analyze sales performance and revenue trends
* Identify top-selling products and categories
* Understand customer purchasing patterns
* Evaluate order and transaction metrics
* Generate actionable business insights

## Dataset

The dataset contains information related to:

* Orders
* Customers
* Products
* Categories
* Sales Revenue
* Quantities Sold
* Order Dates

## Technologies Used

* SQL
* MySQL / PostgreSQL
* Data Analysis
* Aggregate Functions
* Joins and Subqueries
* Window Functions

## Key Analysis Performed

### Sales Analysis

* Total Revenue
* Monthly Sales Trends
* Daily Sales Performance
* Average Order Value

### Product Analysis

* Best-Selling Products
* Top Revenue-Generating Categories
* Product Performance Ranking

### Customer Analysis

* Customer Purchase Frequency
* Top Customers by Revenue
* Customer Retention Insights

### Order Analysis

* Total Orders
* Average Items per Order
* Order Distribution Analysis

## Sample SQL Queries

### Total Revenue

```sql
SELECT SUM(total_amount) AS total_revenue
FROM orders;
```

### Top 10 Products by Sales

```sql
SELECT product_name,
       SUM(quantity) AS total_quantity_sold
FROM sales
GROUP BY product_name
ORDER BY total_quantity_sold DESC
LIMIT 10;
```

### Monthly Revenue Trend

```sql
SELECT MONTH(order_date) AS month,
       SUM(total_amount) AS revenue
FROM orders
GROUP BY MONTH(order_date)
ORDER BY month;
```

## Insights

* Identified top-performing products and categories
* Analyzed customer purchasing behavior
* Evaluated sales growth trends
* Generated business recommendations based on data

## Project Structure

```text
SQL-Zepto-Sales-Analysis/
│
├── dataset/
│   └── zepto_sales.csv
│
├── sql_queries/
│   └── analysis_queries.sql
│
├── screenshots/
│
└── README.md
```

## Learning Outcomes

* SQL Data Analysis
* Data Aggregation Techniques
* Business Intelligence Reporting
* Query Optimization
* Analytical Thinking

## License

This project is for educational and portfolio purposes.
