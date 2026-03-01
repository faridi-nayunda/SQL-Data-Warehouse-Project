# SQL-Data-Warehouse-Project
# 🏗️ Modern SQL Data Warehouse  
### Implementing Medallion Architecture (Bronze 🥉 | Silver 🥈 | Gold 🥇)

---

## 📌 Project Overview

This project demonstrates the design and implementation of a **Modern Data Warehouse** using **Microsoft SQL Server** and the **Medallion Architecture** pattern.

The system transforms raw source data into structured, analytics-ready datasets using a layered approach:

- 🥉 **Bronze Layer** – Raw data ingestion  
- 🥈 **Silver Layer** – Cleaned and standardized data  
- 🥇 **Gold Layer** – Business-ready dimensional models  

The objective is to build a scalable, maintainable, and analytics-driven data platform that supports reporting and business intelligence.

---

## 🎯 Project Goals

- Design a layered data architecture using Medallion principles  
- Implement ETL processes using T-SQL  
- Apply data cleaning and transformation logic  
- Build a Star Schema (Fact & Dimension tables)  
- Enable analytics-ready datasets  
- Demonstrate modern data engineering best practices  

---

## 🏛️ Architecture Overview


Source Systems
↓
🥉 Bronze Layer (Raw Data Storage)
↓
🥈 Silver Layer (Cleaned & Transformed Data)
↓
🥇 Gold Layer (Star Schema & Aggregations)
↓
BI / Reporting / Analytics


---

# 🥉 Bronze Layer – Raw Data

### Purpose
Store raw data exactly as received from source systems.

### Characteristics
- No business transformations applied  
- Preserves original schema  
- Acts as single source of truth  
- Enables reprocessing if needed  

### Example Tables
- `bronze_sales`
- `bronze_customers`
- `bronze_products`

---

# 🥈 Silver Layer – Clean & Structured Data

### Purpose
Improve data quality and prepare datasets for modeling.

### Transformations Applied
- Data type standardization  
- Null handling  
- Duplicate removal  
- Data validation rules  
- Business logic enforcement  
- Derived columns  

### Example Tables
- `silver_sales`
- `silver_customers`
- `silver_products`

This layer ensures consistency and reliability before loading into analytical models.

---

# 🥇 Gold Layer – Business-Ready Warehouse

### Purpose
Provide structured, analytics-ready data using dimensional modeling.

### Design Approach
The Gold layer follows the **Star Schema** design:

- ⭐ Fact Tables (measurable events)
- 📘 Dimension Tables (descriptive attributes)
- 📊 Aggregated Views (KPIs & summaries)

---

## 📊 Data Model

### Fact Table Example

```sql
CREATE TABLE Fact_Sales (
    sale_key INT PRIMARY KEY,
    date_key INT,
    customer_key INT,
    product_key INT,
    quantity INT,
    total_amount DECIMAL(12,2)
);
Dimension Table Example
CREATE TABLE Dim_Customer (
    customer_key INT PRIMARY KEY,
    customer_id INT,
    customer_name VARCHAR(100),
    city VARCHAR(50),
    region VARCHAR(50),
    customer_segment VARCHAR(50)
);
🔄 ETL Process

The ETL workflow was implemented entirely in SQL Server using T-SQL.

Step 1 – Extract

Load raw source data into Bronze tables.

Step 2 – Transform

Clean and standardize data into Silver tables:

Validate fields

Apply business rules

Remove inconsistencies

Step 3 – Load

Populate Fact and Dimension tables in Gold layer.

Step 4 – Serve

Create views and aggregated queries for reporting.

📈 Example Analytical Queries

Total revenue by region

Monthly sales trend analysis

Top 10 products by revenue

Customer segmentation insights

Revenue contribution by product category

🛠️ Technologies Used

Microsoft SQL Server

T-SQL

SQL Server Management Studio (SSMS)

Medallion Architecture

Dimensional Modeling (Star Schema)

Data Warehousing Concepts

📂 Project Structure
/data
/scripts
    ├── 01_bronze_layer.sql
    ├── 02_silver_layer.sql
    ├── 03_gold_layer.sql
    ├── 04_fact_tables.sql
    ├── 05_dimension_tables.sql
    ├── 06_views.sql
/diagrams
README.md
🚀 Key Features

✔️ Medallion Architecture Implementation

✔️ Structured Layered Data Flow

✔️ Data Cleaning & Transformation

✔️ Star Schema Modeling

✔️ Surrogate Key Implementation

✔️ Business-Ready Analytical Models

✔️ Scalable & Maintainable Design

🧠 Skills Demonstrated

Data Warehouse Architecture Design

ETL Development

Data Modeling

SQL Query Optimization

Data Transformation & Cleansing

Business Intelligence Foundations

🔐 Data Quality & Governance

Enforced referential integrity

Applied validation constraints

Structured naming conventions

Layer separation for maintainability

Reproducible transformation logic

🔮 Future Enhancements

Incremental loading strategy

Indexing & performance tuning

Automation using SQL Server Agent

Power BI dashboard integration

Cloud deployment (Azure SQL / Synapse)

CI/CD pipeline integration

📌 Business Value

This project demonstrates how raw operational data can be transformed into a reliable analytics platform that enables:

Data-driven decision making

KPI monitoring

Performance tracking

Trend analysis

Executive reporting

👤 Author

Faridi Nayunda
Data Engineering | Analytics
