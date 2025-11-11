# ecommerce-clickstream-data-engineering-project

## Project Overview

This project demonstrates a **real-world e-commerce analytics pipeline** — from **raw clickstream data ingestion** to **insightful BI dashboards** — using a **Lakehouse architecture built on Azure Databricks**.

The pipeline processes **user activity events** such as *views*, *carts*, and *purchases* to derive key business KPIs like:

- **Conversion Rate**
- **Cart-to-Purchase Rate**
- **User Engagement Metrics**

This end-to-end solution highlights modern data engineering practices, leveraging **Azure Data Lake**, **Databricks Delta Lake**, and **Power BI** for advanced analytics and visualization.

## Architecture

The project follows a **modern Lakehouse architecture** on **Azure Databricks**, designed for scalability, reliability, and real-time insights.

### Key Components

- **Source:** Raw e-commerce clickstream data (CSV files).
- **Storage:** Azure Data Lake Storage Gen2 (ADLS).
- **Compute & Transformation:** Azure Databricks (Bronze → Silver → Gold).
- **Catalog & Governance:** Unity Catalog for centralized metadata and security.
- **Visualization:** Power BI for interactive dashboards.

### Data Flow

1. **Bronze Layer:**  
   - Data is **ingested from GitHub** using **Azure Data Factory** pipelines.  
   - Stored as **raw CSV files** in the *Bronze* container of ADLS.

2. **Silver Layer:**  
   Data cleaned, standardized, and enriched (e.g., splitting `category_code` into multiple levels, fixing timestamps).

3. **Gold Layer:**  
   Aggregated business metrics (KPI calculations such as conversion rate, total purchases, and sessions).

4. **Power BI Dashboard:**  
   Visualizes insights through KPIs, trends, and comparative performance metrics across different time periods.

## Folder Structure

```plaintext
├── src/
│   ├── data/
│   ├── databricks/
│   │   └── notebooks/
│   └── powerbi/
```
## Use Cases

- **Customer Behavior Analysis:** Track user actions (views, carts, purchases) to understand engagement and retention trends.
- **Conversion Funnel Monitoring:** Measure conversion rates and cart-to-purchase ratios to optimize marketing and UX decisions.
- **Performance Benchmarking:** Compare sales and user activity across different time periods.
- **Operational Efficiency:** Enable business teams to visualize insights directly in Power BI for faster decision-making.

## Outcome

A **parameterized data ingestion pipeline** was built using **Azure Data Factory (ADF)** to dynamically load e-commerce clickstream data from GitHub into the **Bronze layer**. The ingested data was then **transformed and enriched in Azure Databricks** using **Unity Catalog** for secure and governed data management. Finally, the **Gold layer** was connected to **Power BI**, enabling interactive dashboards and business insights.

This end-to-end setup represents a **modern Lakehouse architecture** — unifying ingestion, transformation, governance, and analytics in a single ecosystem.
