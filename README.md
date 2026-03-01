# 🏗️ Modern SQL Data Warehouse Project

## 📌 Overview

This project demonstrates the design and implementation of a modern **SQL Server Data Warehouse**. It covers the complete data warehousing lifecycle — from raw data ingestion to dimensional modeling and analytical reporting.

The goal of this project is to transform raw operational data into a structured, analytics-ready data warehouse that supports business intelligence and data-driven decision-making.

---

## 🎯 Objectives

- Design a scalable data warehouse solution  
- Implement ETL (Extract, Transform, Load) processes  
- Apply dimensional modeling (Star Schema)  
- Build fact and dimension tables  
- Enable analytical queries and reporting  
- Optimize performance for large datasets  

---

## 🏛️ Architecture

This project follows the **Medallion Architecture (Bronze–Silver–Gold)** approach to structure data transformation in layers.


Source Data
↓
Bronze Layer (Raw Data)
↓
Silver Layer (Cleaned & Transformed Data)
↓
Gold Layer (Data Warehouse - Star Schema)
↓
Analytics / Reporting


### 🥉 Bronze Layer
- Stores raw data as received from source systems  
- Minimal or no transformations  
- Acts as a historical source of truth  

### 🥈 Silver Layer
- Cleans and validates data  
- Standardizes formats and data types  
- Applies transformation logic and business rules  

### 🥇 Gold Layer
- Contains fact and dimension tables  
- Implements Star Schema design  
- Optimized for analytical queries and reporting  

This layered approach improves maintainability, scalability, and data quality management.

---

## 🛠️ Technologies Used

- Microsoft SQL Server  
- T-SQL  
- SQL Server Management Studio (SSMS)  
- SQL-based ETL processes  
- Dimensional Modeling (Star Schema)  

---

## 📊 Data Modeling

The warehouse is designed using **Dimensional Modeling principles**.

### 🔹 Fact Tables
- Store measurable business metrics  
- Contain foreign keys referencing dimension tables  

Example:

Fact_Sales

Sale_ID
Date_Key
Customer_Key
Product_Key
Amount
Quantity


### 🔹 Dimension Tables
- Store descriptive attributes  
- Enable slicing and dicing of data  

Example:

Dim_Customer

Customer_Key
Customer_Name
City
Region


---

## 🔄 ETL Process

The ETL pipeline includes:

### 1️⃣ Extract
- Extracting raw data into the Bronze layer   
- Preserve source-level structure  

### 2️⃣ Transform
- Cleaning and validating records in the Silver layer  
- Handling missing values and duplicates
- Transforming data types and formats  

### 3️⃣ Load
- Loading structured data into fact and dimension tables (Gold layer) 
- Maintaining referential integrity  
- Populate Fact and Dimension tables  
- Create reporting-ready views

All transformations were implemented using T-SQL.

---

## 📈 Business Value Delivered

The warehouse enables:

- Revenue trend analysis  
- Regional performance tracking  
- Product performance insights  
- Customer segmentation  
- KPI reporting  

The solution transforms raw transactional data into decision-support analytics. 

---

## 🚀 Key Features

✔️ End-to-end data warehouse implementation  
✔️ Medallion layered architecture  
✔️ Star schema design  
✔️ Surrogate key generation  
✔️ Data transformation & cleansing  
✔️ Business-ready analytics queries  
✔️ Scalable and modular structure  

---

## 📂 Project Structure


/data
/scripts
├── create_tables.sql
├── bronze_layer.sql
├── silver_layer.sql
├── gold_layer.sql
├── fact_tables.sql
├── dimension_tables.sql
└── analytics_queries.sql
/diagrams
README.md


---

## 🧠 Skills Demonstrated

- Data Warehouse Architecture Design  
- SQL Development  
- ETL Design & Implementation  
- Dimensional Modeling  
- Query Optimization  
- Business Intelligence Concepts  

---

## 📌 Future Improvements

- Integration with Power BI  
- Automation using SQL Server Agent  
- Incremental data loading strategy (CDC strategy)   
- Performance indexing and partitioning  
- Cloud deployment (Azure SQL / Synapse)
- CI/CD pipeline integration 

---

## 👤 Author

**Faridi Nayunda**  
Data Engineering | Data Analytics
