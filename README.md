
## Databricks S3 Data Pipeline

An end-to-end data consolidation and processing pipeline built using **Amazon S3, Databricks, PySpark, and SQL** to process and consolidate data from **Atlikon and SportsBar** for analysis and reporting.

## Project Overview

This project demonstrates a cloud-based data processing pipeline where data from Atlikon and SportsBar is stored in **Amazon S3** and processed using **Databricks**.

The pipeline is organized into multiple stages, including environment setup, dimension data processing, and fact data processing. It supports both **full-load and incremental-load processing** for fact data.

The processed and consolidated data can then be used for **business analysis and dashboard reporting**.

## Architecture

```text
             Atlikon Data
                  |
             SportsBar Data
                  |
                  v
              Amazon S3
                  |
                  v
              Databricks
                  |
                  v
        Setup and Configuration
                  |
                  v
       Dimension Data Processing
                  |
        +---------+---------+
        |         |         |
        v         v         v
     Customer   Products   Pricing
        |         |         |
        +---------+---------+
                  |
                  v
         Fact Data Processing
                  |
          +-------+-------+
          |               |
          v               v
      Full Load     Incremental Load
          |               |
          +-------+-------+
                  |
                  v
        Consolidated Data
                  |
                  v
             Power BI
             Dashboard
````

## Technologies Used

* **Amazon S3** - Cloud storage for source data
* **Databricks** - Data processing and pipeline development
* **PySpark** - Data transformation and processing
* **SQL** - Data querying and processing
* **Python** - Pipeline development
* **Power BI** - Dashboard and data visualization

## Project Structure

```text
consolidated_pipeline/
|
├── 1_setup/
│   ├── dim_date_table_creation.ipynb
│   ├── setup_catalogs.ipynb
│   └── utilities.ipynb
|
├── 2_dimension_data_processing/
│   ├── 1_customer_data_processing.ipynb
│   ├── 2_products_data_processing.ipynb
│   └── 3_pricing_data_processing.ipynb
|
└── fact_data_processing/
    ├── 1_full_load_fact.ipynb
    └── 2_incremental_load_fact.ipynb
```

## Pipeline Stages

### 1. Setup

The setup stage prepares the Databricks environment and supporting components required for the pipeline.

* **`dim_date_table_creation.ipynb`** - Creates the date dimension required for analysis.
* **`setup_catalogs.ipynb`** - Sets up the required catalogs and data environment.
* **`utilities.ipynb`** - Contains reusable utility functions used during data processing.

### 2. Dimension Data Processing

The dimension processing stage prepares the core reference data required for fact data processing and analysis.

* **`1_customer_data_processing.ipynb`** - Processes customer-related information.
* **`2_products_data_processing.ipynb`** - Processes product-related information.
* **`3_pricing_data_processing.ipynb`** - Processes pricing-related information.

### 3. Fact Data Processing

The fact processing stage handles the main business and transactional data.

* **`1_full_load_fact.ipynb`** - Processes the complete available dataset during a full data load.
* **`2_incremental_load_fact.ipynb`** - Processes newly available or updated data without reprocessing the complete dataset.

## Data Processing Flow

```text
Atlikon + SportsBar Data
          |
      Amazon S3
          |
      Databricks
          |
 Data Ingestion and Processing
          |
 Dimension Data Processing
          |
 Customer ----+
 Products ----+----> Fact Data Processing
 Pricing  ----+
                     |
             Full / Incremental Load
                     |
             Consolidated Data
                     |
                  Power BI
                     |
                 Dashboard
```

## Dashboard

A **Power BI dashboard** is planned to visualize the processed and consolidated Atlikon and SportsBar data.

The dashboard will provide insights into areas such as:

* Customer analysis
* Product performance
* Pricing analysis
* Sales and business performance
* Trends over time
* Key performance indicators (KPIs)

### Dashboard Flow

```text
Databricks Processed Data
          |
       Power BI
          |
     Data Modeling
          |
     KPIs and Measures
          |
     Visualizations
          |
      Dashboard
```

## Key Features

* Integration of data from **Atlikon and SportsBar**
* Cloud-based data storage using **Amazon S3**
* Data processing using **Databricks**
* Data transformation using **PySpark**
* SQL-based data processing
* Date dimension creation
* Customer dimension processing
* Product dimension processing
* Pricing dimension processing
* Full-load fact processing
* Incremental-load fact processing
* Consolidated data for downstream analysis
* Power BI dashboard for visualization

## Project Workflow

1. Source data from Atlikon and SportsBar is stored in Amazon S3.
2. Databricks is used as the data processing environment.
3. Required catalogs and utilities are configured.
4. A date dimension is created.
5. Customer, product, and pricing data are processed.
6. Fact data is processed using full-load and incremental-load approaches.
7. The processed data is consolidated for analysis.
8. The resulting data is used to create a Power BI dashboard.

## Expected Outcome

The project provides a structured pipeline for consolidating Atlikon and SportsBar data and preparing it for analytics.

The combination of **Amazon S3, Databricks, PySpark, SQL, and Power BI** demonstrates an end-to-end workflow from cloud data storage and processing to business intelligence and visualization.

### Technologies

`Python` `SQL` `PySpark` `Databricks` `Amazon S3` `Power BI`
