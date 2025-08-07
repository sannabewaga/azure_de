# 💼 Azure E-Commerce Data Pipeline Project

This project demonstrates an end-to-end cloud data engineering pipeline built on Microsoft Azure, focused on ingesting, transforming, enriching, and visualizing e-commerce data at scale. The architecture follows real-world best practices and showcases how multiple Azure services work together in a production-grade setup.

---

## 🏗️ Architecture Overview



Key Components:
- **Azure Data Factory** for ingestion
- **ADLS Gen2** for scalable storage
- **Azure Databricks** for processing and enrichment
- **MongoDB** for external data enrichment
- **Synapse Analytics** for querying and reporting

---

## 🚀 Implementation Highlights

### 🔄 Data Ingestion
- Ingests data from HTTP endpoints (e.g., GitHub CSVs) and SQL databases
- Pipelines configured with **parameterization** and **dynamic datasets**
- Utilizes **triggered** and **scheduled** pipelines for batch and real-time ingestion
- Error handling and logging implemented for production-readiness

### 💾 Data Storage (Raw Zone)
- Raw data lands in **ADLS Gen2** under structured folder hierarchies
- Organized using **Medallion Architecture** principles (Bronze/Silver/Gold)

### 🧠 Data Transformation & Enrichment
- **Azure Databricks** used for heavy-lift Spark-based transformations
- Implements **cleansing**, **joins**, **aggregations**, and **schema enforcement**
- Integrates with **MongoDB database** to fetch supplementary metadata or enrichment records
- Cleaned and enriched data is written to **Silver** layer in ADLS

### 🧮 Data Serving & Reporting
- Transformed data accessed in **Synapse Analytics** using external tables
- Supports **dedicated** and **serverless** SQL pools for flexible querying
- Final curated tables are moved to the **Gold** layer for business intelligence use
- Visualized using tools like **Power BI**, **Tableau**, or **Microsoft Fabric**

---

## 🛠️ Tools & Technologies

| Service             | Purpose                                  |
|---------------------|------------------------------------------|
| Azure Data Factory  | Data ingestion orchestration             |
| Azure Data Lake Gen2| Scalable storage (Bronze/Silver/Gold)    |
| Azure Databricks    | Data transformation (Apache Spark)       |
| MongoDB Atlas       | NoSQL data enrichment                    |
| Azure Synapse       | Data querying and reporting              |

---

## 📚 Key Learning Outcomes

- Implementing a **real-world Azure Data Engineering pipeline**
- Understanding **Medallion Architecture** in data lakes
- Working with **parameterized pipelines** in ADF
- Integrating **Databricks** with structured and semi-structured data
- Performing **data enrichment** using external NoSQL sources
- Using **Synapse** for cost-effective SQL analysis over lake data

---

## 🧪 Sample Use Cases

- Customer segmentation based on enriched order metadata
- Product performance and return analysis
- Multi-source data consolidation for reporting
- Real-time updates from GitHub-hosted datasets

---



