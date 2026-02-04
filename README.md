# Task 9: SQL Data Modeling — Star Schema

## Overview
This task focuses on building a **Star Schema** for a retail sales dataset, implementing best practices in **data warehousing** and preparing it for **Business Intelligence (BI) analytics**. The project uses the **Global Superstore / E-commerce Orders dataset** to design fact and dimension tables, enabling efficient querying and reporting.

---

## Objective
- Understand the concept of **fact and dimension tables**.
- Design and implement a **Star Schema** in SQL.
- Populate dimensions and fact tables with appropriate keys.
- Run analytics queries to validate schema and data integrity.
- Prepare deliverables for BI reporting.

---

## Tools Used
- **Primary:** PostgreSQL / MySQL  
- **Alternative:** SQLite  
- **Diagramming:** [dbdiagram.io](https://dbdiagram.io/) / [draw.io](https://app.diagrams.net/)  

---

## Dataset
- **Global Superstore Dataset** (Retail Sales / E-commerce Orders)
- Contains transactional data including:
  - Order details, product info, customer info, sales region, and dates.

---

## Steps Completed

1. **Identify Fact & Dimension Tables**
   - **Fact Table:** `sales_fact` (stores transactional metrics like quantity, sales, profit)  
   - **Dimension Tables:**  
     - `customer_dim`  
     - `product_dim`  
     - `date_dim`  
     - `region_dim`

2. **Create Dimension Tables**
   - Added **primary keys** (`customer_id`, `product_id`, `date_id`, `region_id`)
   - Included relevant attributes for each dimension.

3. **Create Fact Table**
   - Included **foreign keys** referencing dimension tables.
   - Included measurable metrics: `quantity`, `sales_amount`, `profit`.

4. **Populate Dimensions**
   - Inserted **distinct values** from source dataset.
   - Surrogate keys used for dimension tables.

5. **Populate Fact Table**
   - Mapped each transaction to **dimension IDs**.
   - Ensured all foreign key relationships are valid.

6. **Create Indexes**
   - Added indexes on all **join keys** to improve query performance.

7. **Run Analytics Queries**
   - Calculated total sales, profit, and quantity by **product, customer, region, and date**.
   - Validated that queries return expected results.

8. **Data Validation**
   - Verified **record counts** between source
