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

##Project structure
consolidated_pipeline/
│
├── 1_setup/
│   ├── dim_date_table_creation.ipynb
│   ├── setup_catalogs.ipynb
│   └── utilities.ipynb
│
├── 2_dimension_data_processing/
│   ├── 1_customer_data_processing.ipynb
│   ├── 2_products_data_processing.ipynb
│   └── 3_pricing_data_processing.ipynb
│
└── fact_data_processing/
    ├── 1_full_load_fact.ipynb
    └── 2_incremental_load_fact.ipynb

##Pipeline Components

1. Setup
The setup stage prepares the environment required for the data pipeline.
Creates the date dimension table
Sets up catalogs
Contains utility functions used throughout the pipeline

2. Dimension Data Processing
The dimension processing stage prepares the core reference data.
Customer Data Processing – Cleans and processes customer information
Products Data Processing – Processes product-related data
Pricing Data Processing – Processes pricing information

3. Fact Data Processing
The fact processing stage handles the main transactional data.
Full Load – Processes the complete dataset
Incremental Load – Processes newly added or updated data without reprocessing the entire dataset
Key Features
Integration of data from Atlikon and SportsBar
Cloud-based data storage using Amazon S3
Data processing using Databricks and PySpark
Dimension and fact data processing
Full-load data processing
Incremental-load data processing
Structured pipeline for consolidated analysis

##Outcome
The pipeline consolidates and transforms data from Atlikon and SportsBar into structured datasets that can be used for downstream analytics and reporting.
