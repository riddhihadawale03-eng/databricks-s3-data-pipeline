# Databricks S3 Data Pipeline

An end-to-end data consolidation pipeline built using **Databricks, PySpark, SQL, and Amazon S3** to process and merge data from **Atlikon and SportsBar** for unified analysis.

## Project Overview

This project processes data from Atlikon and SportsBar using Databricks and Amazon S3. The pipeline performs data ingestion, cleaning, transformation, and consolidation to create structured datasets that can be used for analysis.

## Technologies Used

- **Databricks** – Data processing and pipeline development
- **PySpark** – Data transformation and processing
- **SQL** – Data querying and analysis
- **Amazon S3** – Cloud storage
- **Python** – Pipeline development

## Pipeline Structure

```text
Amazon S3
    ↓
Data Ingestion
    ↓
Data Cleaning & Processing
    ↓
Dimension Data Processing
    ↓
Fact Data Processing
    ↓
Consolidated Data
    ↓
Analysis
