# 📊 Sales Analytics Project – Microsoft Fabric

![Microsoft Fabric](https://img.shields.io/badge/Microsoft%20Fabric-Data%20Analytics-blue)
![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-yellow)
![PySpark](https://img.shields.io/badge/PySpark-Data%20Transformation-orange)
![GitHub](https://img.shields.io/badge/GitHub-Portfolio-black)

## 📌 Projektübersicht

Dieses Projekt zeigt eine vollständige **End-to-End Sales Analytics Lösung** mit **Microsoft Fabric**.

Die Verkaufsdaten werden aus einer CSV-Datei geladen, mit einer automatisierten Pipeline verarbeitet, in der Medallion-Architektur transformiert und anschließend mit Power BI visualisiert.

Das Projekt demonstriert Data Engineering und Business Intelligence Prozesse von der Datenaufnahme bis zum Dashboard.

---

# 🏗️ Architektur

```mermaid
flowchart TD

A[📁 GitHub<br/>sales.csv] --> B[🔄 Microsoft Fabric Pipeline]

B --> C[🥉 Bronze Layer<br/>sales_bronze]

C --> D[🥈 Silver Layer<br/>sales_silver<br/>Cleaning & Transformation]

D --> E[🐍 PySpark Notebook]

E --> F[🥇 Gold Layer]

F --> G[fact_sales]
F --> H[product_summary]
F --> I[customer_summary]
F --> J[date_dim]

G --> K[📊 Semantic Model]
H --> K
I --> K
J --> K

K --> L[📈 Power BI Dashboard]

L --> M[Sales Overview]
L --> N[Product Analysis]
L --> O[Customer Analysis]
```

---

# 🛠️ Technologien

| Technologie | Verwendung |
|---|---|
| Microsoft Fabric | Cloud Data Platform |
| OneLake | Datenspeicherung |
| Data Pipeline | Datenintegration |
| Dataflow Gen2 | Datenbereinigung |
| PySpark | Transformation |
| Delta Lake | Tabellenverwaltung |
| Semantic Model | Datenmodellierung |
| Power BI | Dashboard & Reporting |
| GitHub | Versionskontrolle |

---

# 🔄 Datenprozess (ETL)

## 🥉 Bronze Layer

**sales_bronze**

- Laden der Rohdaten aus GitHub CSV
- Speicherung der Originaldaten

---

## 🥈 Silver Layer

**sales_silver**

Durchgeführte Transformationen:

✅ Prüfung auf Nullwerte  
✅ Entfernung von Duplikaten  
✅ Anpassung der Datentypen  
✅ Berechnung der Spalte `SalesAmount`

---

## 🥇 Gold Layer

Erstellung von Business-optimierten Tabellen:

### fact_sales
- Verkaufsdetails
- Umsatz
- Menge
- Produktinformationen

### product_summary
- Umsatz je Produkt
- Verkaufte Mengen

### customer_summary
- Umsatz je Kunde
- Anzahl Bestellungen

### date_dim
- Jahr
- Quartal
- Monat
- Zeitanalysen

---

# 📊 Power BI Dashboard

Das Dashboard besteht aus drei Seiten:

## 1️⃣ Sales Overview

Enthält:

- Total Revenue
- Total Orders
- Total Quantity
- Sales Trend nach Monat
- Sales nach Produkt


## 2️⃣ Product Analysis

Enthält:

- Total Revenue
- Total Products
- Top Products by Revenue
- Quantity Sold by Product


## 3️⃣ Customer Analysis

Enthält:

- Total Customers
- Customer Revenue
- Top Customers
- Orders by Customer

---

# 📸 Screenshots

## Pipeline

![pipeline](Screenshot 2026-07-14 171349.png)


## Sales Dashboard

![Sales Dashboard](powerbi/sales_dashboard.png)


## Product Analysis

![Product Analysis](powerbi/product_analysis.png)


## Customer Analysis

![Customer Analysis](powerbi/customer_analysis.png)

---

# 📂 Repository Structure

```
Sales-Analytics-Fabric
│
├── sales.csv
│
├── pipeline
│   └── pipeline.png
│
├── notebook
│   └── Gold_Notebook.ipynb
│
├── powerbi
│   ├── sales_dashboard.png
│   ├── product_analysis.png
│   └── customer_analysis.png
│
└── README.md
```

---

# 🚀 Projektergebnisse

✅ End-to-End Datenpipeline  
✅ Medallion Architektur (Bronze/Silver/Gold)  
✅ Datenbereinigung mit Fabric  
✅ Transformation mit PySpark  
✅ Star Schema Datenmodell  
✅ Interaktives Power BI Dashboard  

---

# 👩‍💻 Autor

**Anitha Doddavula**

GitHub: https://github.com/doddavula
