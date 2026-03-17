# End-to-End Data Engineering Project: FMCG M&A Data Consolidation on Databricks (Free Edition)

---

## 🚀 Project Overview

![Project Architecture](project_architecture.png)

This project is an end-to-end Data Engineering pipeline built for a realistic industry use case in the FMCG (Fast-Moving Consumer Goods) domain. The scenario involves a large retail company acquiring a smaller one, and the goal was to build a robust ETL pipeline on the Databricks Free Edition to consolidate data from both companies into a single, unified Lakehouse architecture.

This project is designed for both beginners and advanced users looking to understand modern data engineering practices using a powerful tech stack.

---

## 🎯 The Business Problem: M&A Data Consolidation

When a big company acquires a smaller one, a critical challenge is merging their data landscapes.

This project simulates two separate data sources:

- **Big Retailer:** Historical sales data  
- **Small Company:** Recent sales data  

The objective was to build a pipeline that ingests, cleans, transforms, and enriches this combined data to provide a single source of truth for business analysis.

---

## 🛠️ Tech Stack & Tools

- **Cloud Storage:** Amazon S3  
- **Data Processing:** Apache Spark  
- **Platform:** Databricks (Free)  
- **Language:** Python (PySpark), SQL  
- **Architecture:** Medallion Architecture (Bronze, Silver, Gold)  
- **Orchestration:** Databricks Notebooks  
- **BI & Reporting:** Databricks SQL Dashboard & Genie  

---

## 🏗️ Architecture Diagram

![Project Architecture](project_architecture.png)

---

## 📂 Project Structure

```
End-to-End-Data-Engineering-Databricks-FMCG

├── data/
│   ├── parent_company/
│   │   ├── full_load/
│   │   └── incremental_load/
│   │
│   ├── child_company/
│       ├── full_load/
│       └── incremental_load/

├── notebooks/
│   ├── 01_setup/
│   ├── 02_dimension_processing/
│   ├── 03_fact_processing/

├── dashboards/
│   └── (Power BI / BI files)

├── resources/
│   └── (architecture diagrams, images, docs)

├── README.md

```

---

## 📝 Step-by-Step Pipeline Implementation

### 1. Bronze Layer: Raw Data Ingestion

- Uploaded raw CSV files to Amazon S3  
- Loaded data into Bronze Delta tables using PySpark  
- Maintained raw, immutable data  

---

### 2. Silver Layer: Data Cleansing & Transformation

- Standardized schemas and column names  
- Handled null values and removed duplicates  
- Created derived columns (year, month, quarter)  

Output: Clean, structured Silver Delta tables  

---

### 3. Gold Layer: Business-Level Aggregation

- Sales by product category  
- Top performing stores  
- Monthly sales trends  

Output: Aggregated, analytics-ready Gold tables  

---

### 4. Reporting & Analysis

- Built dashboards using Databricks SQL  
- Explored Genie for conversational queries  

Example:
> “What were the top 5 selling products last month?”

---

## ⚙️ How to Run This Project

### Prerequisites

- Databricks Community Edition account  
- AWS S3 bucket (or DBFS alternative)  

### Setup

1. Clone repository  
2. Upload CSV files to S3 or DBFS  

### Execution

1. Import notebooks into Databricks  
2. Update file paths in ingestion notebook  
3. Run notebooks in order:
   - Bronze → Silver → Gold  
4. Build dashboard using Gold tables  

---

## 💡 Key Learnings

- Built a Medallion Architecture from scratch  
- Used PySpark for distributed processing  
- Simulated real-world M&A data consolidation  
- Delivered business-ready analytics outputs  
- Leveraged Databricks Free Edition effectively  

---

## 🙏 Credits

This project was inspired by the tutorial from **codebasics**: 

---

# 📫 Contact

## Oluwatosin Amosu Bolaji 
- Data Engineer 
- Buiness Intelligence Analyst
- ETL Developer

#### 🚀 **Always learning. Always building. Data-driven to the core.**  

### 📫 **Let’s connect!**  
- 📩 oluwabolaji60@gmail.com
- 🔗 : [LinkedIn](https://www.linkedin.com/in/oluwatosin-amosu-722b88141)
- 🌐 : [My Portfolio](https://www.datascienceportfol.io/oluwabolaji60) 
- 𝕏 : [Twitter/X](https://x.com/thee_oluwatosin?s=21&t=EqoeQVdQd038wlSUzAtQzw)
- 🔗 : [Medium](https://medium.com/@oluwabolaji60)
- 🔗 : [View my Repositories](https://github.com/Tbrown1998?tab=repositories)
