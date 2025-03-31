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
