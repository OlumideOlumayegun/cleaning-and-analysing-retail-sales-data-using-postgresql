# Cleaning and Analysing Retail Sales Data Using PostgreSQL

![banner image](/images/banner_image.png)

## Project Overview

This project focuses on cleaning and analysing retail sales data using PostgreSQL. The dataset represents transactional records from a Super Store business and includes information about customer orders, products, sales performance, discounts, profits, and returns.

The main objective of the project is to apply SQL techniques commonly used by data scientists and data analysts to solve real-world business problems involving:

- Data cleaning
- Missing value imputation
- Product performance analysis
- Sales aggregation
- Ranking and window functions
- Relational database querying

The project demonstrates how SQL can be used not only for querying databases but also for preparing high-quality datasets for business intelligence and machine learning workflows.

---

## Project Tasks

### Task 1 — Top Performing Products Analysis

Identify the top five products from each category based on highest total sales.

#### Objectives
- Aggregate product sales and profit
- Rank products within categories
- Use SQL window functions
- Generate category-level business insights

#### SQL Concepts Used
- `JOIN`
- `GROUP BY`
- `SUM()`
- `RANK()`
- `PARTITION BY`
- `ORDER BY`
- `Subqueries`

---

### Task 2 — Missing Quantity Value Imputation

Estimate missing quantity values in the `orders` table using calculated unit prices derived from existing sales records.

#### Objectives
- Detect missing values
- Calculate unit prices
- Estimate missing quantities
- Improve data quality

#### SQL Concepts Used
- `Common Table Expressions (CTEs)`
- `CAST()`
- `ROUND()`
- `Conditional filtering`
- `Data imputation logic`
- `Multi-column joins`

---

## Dataset Description

The project uses a retail Super Store database consisting of four relational tables.

### 1. Orders Table

Contains transactional sales data.

| Column | Description |
|---|---|
| row_id | Unique record identifier |
| order_id | Unique order identifier |
| order_date | Date order was placed |
| market | Market associated with the order |
| region | Customer region |
| product_id | Purchased product ID |
| sales | Total sales amount |
| quantity | Quantity purchased |
| discount | Applied discount |
| profit | Profit earned |

---

### 2. Products Table

Contains product information and categories.

| Column | Description |
|---|---|
| product_id | Product identifier |
| category | Product category |
| sub_category | Product sub-category |
| product_name | Product name |

---

### 3. Returned Orders Table

Contains returned order information.

| Column | Description |
|---|---|
| returned | Return indicator |
| order_id | Returned order ID |
| market | Associated market |

---

### 4. People Table

Contains salesperson and regional information.

| Column | Description |
|---|---|
| person | Salesperson name |
| region | Operating region |

---

## Technologies Used

- PostgreSQL
- SQL
- Window Functions
- Common Table Expressions (CTEs)

---

## Skills Demonstrated

- SQL Data Cleaning
- Data Transformation
- Data Aggregation
- Ranking and Window Functions
- Missing Data Handling
- Relational Database Querying
- Analytical Problem Solving
- Business Intelligence Analysis

---

## Project Structure

```text
├── README.md
├── requirements.txt
├── analysing-sales-data.ipynb
├── create_postgresql_db_tables.ipynb
├── images/
└── dataset/
```

---

## Sample SQL Features Used

### Window Function Example

```sql
RANK() OVER (
    PARTITION BY category
    ORDER BY SUM(sales) DESC
)
```

### Common Table Expression Example

```sql
WITH missing AS (
    SELECT *
    FROM orders
    WHERE quantity IS NULL
)
```

---

## Key Insights

- High-performing products were identified across multiple categories.
- Sales and profitability trends were analysed using SQL aggregation.
- Missing quantity values were successfully estimated using pricing patterns.
- The project demonstrated practical approaches to real-world data quality challenges.

---

# Conclusion

This project showcased how PostgreSQL and SQL can be used for end-to-end retail data cleaning and analysis. Through ranking analysis and missing value imputation, the project demonstrated practical SQL techniques widely used in data science, analytics, and business intelligence workflows.

The project also strengthened foundational skills in:
- Data preprocessing
- Relational database analysis
- Query optimization
- Business reporting
- Analytical thinking

---

# Author

Olumide Olumayegun


````
