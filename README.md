# 📊 Sales Analytics Project - Microsoft Fabric

## 📌 Project Overview

This project demonstrates an end-to-end **Sales Analytics solution** using **Microsoft Fabric**.

The sales data is loaded from a CSV file, processed through a Medallion Architecture (Bronze, Silver, Gold), and visualized using Power BI dashboards.

---

## 🛠️ Technologies Used

- Microsoft Fabric
- OneLake
- Data Pipeline
- Dataflow Gen2
- PySpark Notebook
- Delta Lake
- Semantic Model
- Power BI
- GitHub

---

## 🏗️ Architecture

```
GitHub (sales.csv)
        |
        v
Microsoft Fabric Pipeline
        |
        v
Bronze Layer
(sales_bronze)
        |
        v
Silver Layer
(sales_silver)
(Data Cleaning & Transformation)
        |
        v
PySpark Notebook
        |
        v
Gold Layer
        |
        +----------------+
        |                |
   fact_sales     product_summary
        |
   customer_summary
        |
      date_dim
        |
        v
Fabric Semantic Model
        |
        v
Power BI Dashboard
```

---

## 🔄 Data Processing

### Bronze Layer

- Loaded raw sales CSV data into Fabric Lakehouse
- Stored original source data

### Silver Layer

Data cleaning steps:

- Checked null values
- Removed duplicates
- Changed data types
- Created SalesAmount column

### Gold Layer

Created analytical tables:

**fact_sales**
- Sales transactions
- Quantity
- Revenue

**product_summary**
- Sales by product
- Product performance

**customer_summary**
- Customer revenue
- Customer orders

**date_dim**
- Year
- Quarter
- Month analysis

---

## 📈 Power BI Dashboard

The dashboard contains three pages:

### 1. Sales Overview

- Total Revenue
- Total Orders
- Total Quantity
- Sales Trend by Month
- Sales by Product

### 2. Product Analysis

- Total Revenue
- Total Products
- Top Products by Revenue
- Quantity Sold by Product

### 3. Customer Analysis

- Total Customers
- Customer Revenue
- Top Customers
- Orders by Customer

---

## 📸 Screenshots

### Microsoft Fabric Pipeline

![Pipeline](pipeline/pipeline.png)


### Sales Dashboard

![Sales Dashboard](powerbi/sales_dashboard.png)


### Product Analysis

![Product Analysis](powerbi/product_analysis.png)


### Customer Analysis

![Customer Analysis](powerbi/customer_analysis.png)

---

## 📂 Repository Structure

```
Sales-Analytics-Fabric
|
|-- sales.csv
|
|-- pipeline
|   |-- pipeline.png
|
|-- notebook
|   |-- Gold_Notebook.ipynb
|
|-- powerbi
|   |-- sales_dashboard.png
|   |-- product_analysis.png
|   |-- customer_analysis.png
|
|-- README.md
```

---

## 🚀 Project Highlights

✅ End-to-end ETL pipeline  
✅ Medallion Architecture (Bronze/Silver/Gold)  
✅ Data cleaning and transformation  
✅ PySpark data processing  
✅ Data modeling with Semantic Model  
✅ Interactive Power BI dashboards  

---

## 👩‍💻 Author

**Anitha Doddavula**

GitHub: https://github.com/doddavula
