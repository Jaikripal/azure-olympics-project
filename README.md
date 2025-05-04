# 🏅 End-to-End Azure Data Engineering Pipeline – Olympics 2024 (Interview Project)

This project demonstrates my ability to design and implement a **scalable, production-ready data engineering solution** using modern Azure technologies. It simulates a real-world use case of processing and transforming **Olympics 2024 event data** using **Medallion Architecture** with **orchestration, transformation, and CI/CD**.

---

## 🧩 Use Case (Business Scenario)

**Objective:**  
To build a robust data pipeline for the **Olympics 2024 Committee** to process, clean, transform, and analyze data from various sources (such as athlete stats, event schedules, and medal tallies). The goal is to power dashboards and analytics for performance monitoring, reporting, and fan engagement.

**Challenges Addressed:**
- Ingesting raw Excel files daily from source systems
- Cleaning and transforming semi-structured data (nulls, duplicates)
- Creating a historical, query-optimized data warehouse layer
- Enabling self-serve analytics and BI reporting in Azure Synapse

---

## 🚀 Key Highlights

| Area                  | Tech Stack / Tool                                |
|-----------------------|--------------------------------------------------|
| Orchestration         | Azure Data Factory (ADF)                         |
| Transformation        | Databricks (PySpark) + Delta Live Tables (DLT)  |
| Storage               | Azure Data Lake Gen2                            |
| Data Warehouse        | Azure Synapse Analytics                         |
| CI/CD Automation      | Azure DevOps (ADF + Databricks deployment)      |
| Architecture Pattern  | Medallion Architecture (Bronze/Silver/Gold)     |

---

## 🧱 Project Architecture

![Architecture Diagram](architecture/pipeline-diagram.png)

**Flow:**

1. **ADF** ingests raw Excel/CSV files into Bronze layer in **Data Lake Gen2**
2. **Databricks Notebooks** process and clean Bronze data into structured Silver data
3. **Delta Live Tables (DLT)** aggregate and prepare Gold layer for reporting
4. **Synapse Analytics** consumes Gold data for dashboards and BI tools
5. **Azure DevOps** automates CI/CD of notebooks, ADF pipelines, and DLT configs

---

## 🔗 Medallion Architecture

| Layer   | Description                                            | Example Fields                     |
|---------|--------------------------------------------------------|------------------------------------|
| Bronze  | Raw ingestion from source files                        | athlete_id, name, raw_event_data   |
| Silver  | Cleaned & validated data with schema enforcement       | athlete_id, event, score, country  |
| Gold    | Aggregated insights for visualization & analytics      | top_athletes, medal_count_by_team  |

---

## 📂 Repository Structure

```
📦 azure-olympics-2024-pipeline
├── README.md                    # Project overview
├── architecture/               # System diagram
│   └── pipeline-diagram.png
├── notebooks/                  # Databricks notebooks
│   ├── bronze_layer_processing.ipynb
│   ├── silver_layer_transformations.ipynb
│   └── gold_layer_aggregation.ipynb
├── delta_live_tables/          # SQL DLT logic
│   ├── dlt_bronze.sql
│   ├── dlt_silver.sql
│   └── dlt_gold.sql
├── adf/                        # Azure Data Factory pipeline artifacts
│   ├── pipeline_export.json
│   └── linked_services.json
├── devops/                     # Azure DevOps CI/CD scripts
│   └── azure-pipelines.yml
├── datasets/                   # Sample data
│   └── olympics_2024_raw_data.csv
└── LICENSE
```

---

## 💡 What I Learned

- How to implement **Delta Lake best practices** in Databricks
- Efficiently **schedule and retry pipelines** in ADF
- Automate deployment using **CI/CD in Azure DevOps**
- Layered storage and **schema evolution handling**
- Building pipelines with **scalability, fault tolerance, and modularity**

---

## 🧪 Possible Extensions (If Given More Time)

- Real-time streaming ingestion using **Event Hubs + Databricks Structured Streaming**
- Data Quality checks with **Great Expectations**
- Role-based access control using **Unity Catalog**
- Integration with **Power BI dashboards** from Synapse

---

## 📊 Target Audience

This project is ideal for:

- **Interview demonstrations** (mid-to-senior Azure Data Engineer roles)
- **Showcasing architectural thinking**
- Proving **hands-on cloud skills** with production-ready tooling

---

## 📬 Contact

- **LinkedIn**: [Your Profile](#)
- **Instagram**: [Your Page](#)
- **Email**: youremail@example.com

---

> 🔒 **Disclaimer**: This project is based on publicly available mock data and is for demonstration and educational purposes only.
