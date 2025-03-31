# 💡 Azure Data Engineering Project – Olist E-Commerce Dataset

## 📌 Overview

This project demonstrates an end-to-end big data pipeline using **Microsoft Azure** services to ingest, transform, enrich, and visualize large-scale e-commerce data from the Brazilian Olist marketplace. It integrates structured and unstructured data from **GitHub**, **MySQL**, and **MongoDB** sources, employing **Azure Data Factory**, **Databricks (PySpark)**, **ADLS Gen2**, **Synapse Analytics**, and **Power BI** for business insights and predictive analysis.

---

## 🚀 Architecture

The pipeline follows the data lakehouse paradigm and consists of:

- **Data Sources**: GitHub, MySQL (structured), and MongoDB (NoSQL)
- **Ingestion**: Azure Data Factory with parameterized JSON pipelines
- **Storage**: ADLS Gen2 with Delta Lake (Bronze → Silver → Gold)
- **Transformation**: PySpark in Azure Databricks
- **Enrichment**: MongoDB tables joined during transformation
- **Visualization**: Power BI via Synapse SQL views

![Project Architecture](https://github.com/SYEDFAIZAN1987/BigDataEngineeringProject/blob/main/ProjectArchitecture.png)

---

## 📂 Data Sources

The project uses the **Olist e-commerce dataset**, which includes:
- Customers
- Orders
- Sellers
- Payments
- Products
- Reviews
- Geolocation

The complete data schema and relational joins are visualized below:

![Entity Relationship Diagram](https://github.com/SYEDFAIZAN1987/BigDataEngineeringProject/blob/main/1dataschema.png)

---

## 📊 Exploratory Analysis & Visualizations

Key KPIs and metrics were computed using PySpark and visualized in Power BI:

- **Average Delivery Delay**
- **Top Product Categories by Revenue**
- **Freight vs Payment Value Trends**
- **Customer Engagement by Region**
- **Correlation Matrix (Pearson)**
- **Delivery Timeliness by State**

| Delay vs Freight | Sales by Category |
|------------------|-------------------|
| ![ana1](https://github.com/SYEDFAIZAN1987/BigDataEngineeringProject/blob/main/ana1.png) | ![ana2](https://github.com/SYEDFAIZAN1987/BigDataEngineeringProject/blob/main/ana2.png) |

---

## 📈 Dashboard Insights (Power BI)

- Order trends across time and states
- Payment behavior and freight distribution
- KPI tiles summarizing key metrics
- Top categories and sellers
- Delivery estimates vs actuals

![Power BI Dashboard Page 1](https://github.com/SYEDFAIZAN1987/BigDataEngineeringProject/blob/main/page_1.png)
![Dashboard Page 2](https://github.com/SYEDFAIZAN1987/BigDataEngineeringProject/blob/main/page_2.png)
![Dashboard Page 3](https://github.com/SYEDFAIZAN1987/BigDataEngineeringProject/blob/main/page_3.png)
![Dashboard Page 4](https://github.com/SYEDFAIZAN1987/BigDataEngineeringProject/blob/main/page_4.png)
![Dashboard Page 5](https://github.com/SYEDFAIZAN1987/BigDataEngineeringProject/blob/main/page_5.png)
![Dashboard Page 9](https://github.com/SYEDFAIZAN1987/BigDataEngineeringProject/blob/main/page_9.png)
![Dashboard Page 10](https://github.com/SYEDFAIZAN1987/BigDataEngineeringProject/blob/main/page_10.png)

---

## 📁 Repository Structure

- `*.csv`: Raw Olist dataset files
- `*.ipynb`: Databricks notebooks with PySpark transformations
- `*.json`: Parameterized ingestion configurations
- `SQLScripts/`: Synapse scripts to create views and load tables
- `PowerBI/`: Power BI report files and screenshots

---

## 🔐 Technologies Used

- **Azure Data Factory**
- **Azure Databricks (PySpark)**
- **Azure Data Lake Gen2**
- **Azure Synapse Analytics**
- **Power BI**
- **MySQL (via Files.io)**
- **MongoDB (NoSQL Enrichment)**
- **GitHub for Version Control**

---

## 📜 SQL Scripts

- [Create Views](https://github.com/SYEDFAIZAN1987/BigDataEngineeringProject/blob/main/SynapseSQLcodetoCreateTableViews)
- [Load Gold Layer](https://github.com/SYEDFAIZAN1987/BigDataEngineeringProject/blob/main/SynapseSQLcodetoloadGoldLayer)
- [Synapse Workspace](https://github.com/SYEDFAIZAN1987/BigDataEngineeringProject/blob/main/SynapseWorkspace)

---



## 👨‍💻 Author
**Syed Faizan**  
📅 March 28, 2025

---

## 📚 Table of Contents
1. [Introduction](#introduction)
2. [Project Summary](#project-summary)
3. [Architecture Overview](#architecture-overview)
4. [Repository and Data Sources](#repository-and-data-sources)
5. [Data Lake Zones and Pipelines](#data-lake-zones-and-pipelines)
6. [Power BI Dashboard](#power-bi-dashboard)
7. [Exploratory Data Analysis](#exploratory-data-analysis)
8. [Insights and Advanced Analytics](#insights-and-advanced-analytics)
9. [Results and Conclusions](#results-and-conclusions)
10. [References](#references)

---

## 📌 Introduction
This project explores a large-scale e-commerce dataset from the Olist platform using tools from the Azure ecosystem. It involves data ingestion, transformation, enrichment, and visualization to identify trends, inefficiencies, and correlations for business insights.

---

## 📦 Project Summary
- Addressed logistics inefficiencies using transactional and behavioral e-commerce data
- Used Azure ADF, Databricks (PySpark), ADLS Gen2, Synapse Analytics, and Power BI
- Integrated MySQL and MongoDB data sources
- Identified delays, freight-payment correlations, seller performance, and state-level disparities

---

## 🏗️ Architecture Overview
A data lakehouse pipeline was built using:
- **Ingestion**: ADF with JSON configs from GitHub and SQL sources
- **Storage**: ADLS Gen2 with Bronze/Silver/Gold layers
- **Transformation**: Azure Databricks with PySpark
- **Serving**: Azure Synapse SQL and Power BI

---

## 🔗 Repository and Data Sources
- GitHub hosts CSV data files
- Filess.io supports hybrid SQL (MySQL) and NoSQL (MongoDB)
- Normalized ERD ensures relational joins for OLAP and ETL operations

---

## 🗂️ Data Lake Zones and Pipelines
- **Bronze Layer**: Raw CSVs stored in Blob Storage
- **Silver Layer**: Cleaned & transformed records
- **Gold Layer**: Aggregated, curated datasets for BI
- ADF uses Lookup-ForEach-Copy with JSON parameters

---

## 📊 Power BI Dashboard
- KPIs: Avg Delay, Avg Payment, Product/Customer Count
- State-wise delivery & payment comparisons
- Trendlines, scatterplots, heatmaps for visual storytelling

---

## 📈 Exploratory Data Analysis
- **Top Delay Categories**: Fashion clothing, Cine photo
- **Top Revenue Categories**: Bed bath table, Health beauty
- **Most Used Payment**: Credit cards (87,776)
- **High Customer States**: SP, RJ, MG
- **Best Rated**: CDs/DVDs, Books

---

## 🔬 Insights and Advanced Analytics
- Freight value ↑ leads to early delivery
- More product images → lower delay
- Delay ~ correlated with delivery estimates
- Geographic disparities in delay and freight cost
- High-value items → more payment installments
- Negative delays common across Brazil

---

## ✅ Results and Conclusions
- Actual deliveries were much faster than estimates (up to 37 days earlier)
- Freight value (r = 0.74) and product value are strongly correlated
- Top product categories and high-revenue sellers were identified
- Consistent delivery improvements from 2016–2018
- 97.13% orders were successfully delivered
- Recommendations: dynamic freight pricing, better metadata, predictive delivery modeling

---

## 📚 References
- Chapman, G. (2016). *Data analysis for business, economics, and policy*. Springer.
- Chen, H. et al. (2012). *MIS Quarterly*, 36(4), 1165–1188.
- Microsoft Docs (2023). [Azure Data Factory Documentation](https://learn.microsoft.com/en-us/azure/data-factory/introduction)
- Gandomi & Haider (2015). *Int. J. of Information Management*, 35(2), 137–144.
"""




## 📚 Author

**Syed Faizan**  
MPS in Analytics – Applied Machine Learning  
Northeastern University  
📍 Toronto, Ontario, Canada  
✉️ faizan.s@northeastern.edu

---

## 📌 Citation & References

- Microsoft Docs: [Azure Data Factory](https://learn.microsoft.com/en-us/azure/data-factory/introduction)
- Databricks Delta Lake: [Delta Architecture](https://www.databricks.com/delta)
- Kaggle: Olist E-commerce Dataset
- Gandomi & Haider (2015). Beyond the hype: Big data concepts, methods, and analytics.
