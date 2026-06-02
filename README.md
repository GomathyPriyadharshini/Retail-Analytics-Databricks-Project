# Retail Databricks Analytics Project

## Overview

This project demonstrates an end-to-end retail data analytics pipeline using Databricks and PySpark. The solution follows a Medallion Architecture (Bronze → Silver → Gold) to ingest, clean, transform, and analyze retail sales data.

The project showcases data engineering concepts, Spark SQL analytics, data transformation techniques, and business intelligence reporting using Databricks Community Edition.

---

## Business Problem

Retail organizations generate large volumes of transactional data that require processing before meaningful business insights can be derived.

The objective of this project is to:

* Ingest raw retail sales data
* Clean and standardize records
* Build curated analytical datasets
* Generate business insights using Spark SQL
* Demonstrate modern data engineering practices

---

## Tech Stack

* Databricks Community Edition
* Apache Spark
* PySpark
* Spark SQL
* Delta Tables
* GitHub
* Draw.io

---

## Project Architecture

```text
                    +------------------+
                    |  Retail Dataset  |
                    |   CSV / Kaggle   |
                    +--------+---------+
                             |
                             v
                    +------------------+
                    | Bronze Layer     |
                    | Raw Data Ingest  |
                    +--------+---------+
                             |
                             v
                    +------------------+
                    | Silver Layer     |
                    | Data Cleaning    |
                    | Null Handling    |
                    | Deduplication    |
                    +--------+---------+
                             |
                             v
                    +------------------+
                    | Gold Layer       |
                    | Business Metrics |
                    | Customer KPIs    |
                    | Product KPIs     |
                    +--------+---------+
                             |
                             v
                    +------------------+
                    | Spark SQL        |
                    | Analytics        |
                    | Reporting        |
                    +------------------+
```

---

## Repository Structure

```text
Retail-Databricks-Analytics/
│
├── notebooks/
│   ├── 01_bronze_online_retail_ingestion.py
│   ├── 02_silver_online_retail_transformation.py
│   └── 03_gold_online_retail_business_metrics.py
│   └── 04_Analytics_queries.py
│
├── datasets/
│   └── online_retail.csv
│
├── screenshots/
│
├── architecture/
│   └── architecture.png
│
└── README.md
```

---

## Dataset

The data used in this project is based on the Online Retail Dataset obtained from Kaggle. The source dataset contains approximately 3 million rows of transactional retail data.

Due to GitHub repository size limitations and to maintain a streamlined development experience, the complete dataset is not stored in this repository. Instead, a representative sample dataset is included to demonstrate the end-to-end data engineering workflow, including ingestion, transformation, data quality validation, and analytical reporting.

All transformations and processing logic have been designed to operate on the full dataset without modification.

## Data Pipeline

### Bronze Layer

Raw retail dataset is loaded into Databricks from CSV files.

Activities:

* Data ingestion
* Schema validation
* Initial profiling

### Silver Layer

Data cleansing and standardization.

Transformations:

* Remove duplicate records
* Handle null values
* Standardize data types
* Remove invalid transactions
* Data quality checks

### Gold Layer

Business-ready datasets created for analytics.

Metrics generated:

* Customer spending
* Product revenue
* Country-wise sales
* Monthly revenue trends

---

## Analytics Performed

### 1. Top Revenue-Generating Product by Country

Identifies the highest revenue-generating product in each country.

### 2. Monthly Revenue Trend Analysis

Tracks monthly revenue performance over time.

### 3. Customer Spending vs Country Average

Compares individual customer spending against country averages.

### 4. Top 3 Customers by Spending in Each Country

Ranks customers based on total spending within each country.

### 5. Month-over-Month Revenue Analysis

Measures revenue growth and decline using window functions.

---

## Key Spark Concepts Demonstrated

### Data Engineering

* Data Ingestion
* Data Cleaning
* Data Transformation
* Medallion Architecture
* ETL Pipeline Development

### Spark SQL

* Aggregations
* Window Functions
* DENSE_RANK()
* LAG()
* GROUP BY
* Common Table Expressions (CTEs)

### PySpark

* DataFrame Operations
* Schema Management
* Null Handling
* Filtering and Transformations

---

## Sample Business Insights

* Identified top-performing products by country.
* Analyzed monthly sales trends.
* Ranked highest-value customers.
* Compared customer spending against regional averages.
* Evaluated month-over-month revenue changes.

---

## Screenshots

Add screenshots in the `/screenshots` folder:

* Bronze Layer Processing
* Silver Layer Transformations
* Gold Layer Tables
* Spark SQL Queries
* Analytics Outputs
* Databricks Workspace

Example:

```text
screenshots/
├── bronze_layer.png
├── silver_layer.png
├── gold_layer.png
├── monthly_revenue.png
├── top_products.png
└── customer_analysis.png
```

---

## Learning Outcomes

Through this project, I gained experience in:

* Building data pipelines using Databricks
* Implementing Medallion Architecture
* Performing data transformations with PySpark
* Writing analytical queries using Spark SQL
* Creating portfolio-ready data engineering projects
* Version control using GitHub

---

## Future Enhancements

* Delta Live Tables
* Databricks Workflows
* Incremental Data Loads
* Data Quality Framework
* Power BI Dashboard Integration
* Azure Data Lake Integration
* Real-Time Streaming Analytics

---

## Author

Data Engineering Portfolio Project

Built using Databricks Community Edition, PySpark, and Spark SQL.
