# Spotify-Azure-Databricks-Project


---

# Azure Data Project Architecture

## Overview

 The goal is to build a full-fledged **data engineering pipeline** with modern industry practices, including incremental processing, backfilling, streaming data, and metadata-driven pipelines.
---

## Project Architecture

![Project Architecture](images/arc.jpg)

The project follows the **Medallion Architecture** (Bronze → Silver → Gold) with the following flow:

1. **Source**

   * Primary source: **Azure SQL Database** (cloud-hosted)
   * Secondary source (optional): **GitHub repository** for static files
   * Purpose: Provide raw data for the pipeline

2. **Bronze Layer**

   * Tool: **Azure Data Factory**
   * Function: Load raw data into the Bronze layer
   * Features:

     * Incremental data load
     * Parameterized and dynamic pipelines
     * Git integration for CI/CD
   * Significance: Data remains raw, ready for processing in Silver layer

3. **Silver Layer**

   * Tool: **Azure Databricks**
   * Function: Process and enrich data
   * Features:

     * Learn and use the latest Databricks frameworks
     * Spark Structured Streaming and AutoLoader
     * Unity Catalog, metastore, credentials, external locations
     * Metadata-driven notebooks and pipelines
     * Star schema modeling and slowly changing dimensions
   * Significance: Transforms raw data into structured and enriched data

4. **Gold Layer**

   * Tool: **Delta Live Tables (Azure Databricks)**
   * Function: Build final curated models
   * Features:

     * CI/CD using Databricks Asset Bundles
     * Ready for dashboards or sharing endpoints with other teams
   * Significance: Provides clean, production-ready data

---

## Key Concepts Covered

* **Incremental Processing:** Process data in small increments rather than bulk
* **Backfilling:** Fill missing data for specific intervals
* **Streaming Data:** Real-time data processing using Spark Structured Streaming
* **Custom Utilities:** Python classes and functions reusable across pipelines
* **Metadata-Driven Pipelines:** Build dynamic pipelines controlled by metadata
* **Star Schema & Slowly Changing Dimensions:** Standard dimensional modeling in data warehousing
* **Git & CI/CD Integration:** Collaborate efficiently and deploy pipelines reliably

---

## Learning Outcomes

By completing this project, you will learn:

* How to architect a data pipeline from scratch
* How to use Azure SQL Database as a cloud source
* How to build robust Bronze → Silver → Gold pipelines
* How to work with modern Azure Databricks features
* How to implement metadata-driven solutions in real-world scenarios
* How to apply CI/CD principles in Azure Databricks projects
* How to prepare your data for dashboards or analytics teams

---

## Project Requirements

* Incremental data processing (no bulk processing)
* Backfilling support
* Stream processing with Spark
* Integration of custom Python utilities
* Git-based collaboration for pipelines

---

## Next Steps

1. Set up **Azure SQL Database** as the source
2. Load data into **Bronze layer** via Azure Data Factory
3. Process and enrich data in **Silver layer** using Azure Databricks
4. Curate final datasets in **Gold layer** with Delta Live Tables
5. Share endpoints with dashboards or other teams

---

This README gives a **clear blueprint of the project**, making it easy for anyone to understand the flow, tools, and purpose of each layer.

---

لو تحب، أقدر أعمل لك نسخة **مرئية وجذابة أكتر بالـ Markdown** تشمل **diagrams** لكل طبقة (Bronze, Silver, Gold) بحيث تظهر كـ architecture diagram داخل README، وده هيخلي المشروع **احترافي أكتر على GitHub**.

تحب أعملهولك كده؟
