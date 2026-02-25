🚀 Project 1 – Enterprise-Grade Customer Account Data Pipeline (Azure)
📌 Overview

This project demonstrates the design and implementation of a production-ready Azure data pipeline built using modern cloud data engineering principles.

The solution ingests raw banking datasets, processes them through a multi-layered architecture (Bronze → Silver → Gold), and delivers curated data into Azure SQL Database for analytics and reporting.

Designed with scalability, modularity, and enterprise best practices in mind.

🏗 Architecture Overview
ETL Workflow

The architecture follows the Medallion Design Pattern:

Bronze Layer (Raw) – Immutable raw ingestion

Silver Layer (Cleaned) – Standardized & validated datasets

Gold Layer (Curated) – Business-ready structured data

🎯 Business Objective

Build a scalable Azure-based ETL framework to:

Ingest customer banking datasets from backend storage

Perform cleansing and schema standardization

Apply business transformations including SCD logic

Load curated data into Azure SQL Database

Enable downstream reporting in Power BI

🔄 End-to-End Data Engineering Workflow
🟤 Step 1: Data Ingestion (Source → Bronze Layer)

Source

Local File System

Files:

accounts.csv

customers.csv

loan_payments.csv

loans.csv

transactions.csv

Dataset Reference
AI Bank Dataset (Kaggle)

Process

Built parameterized ADF pipelines

Ingested raw files into Azure Data Lake Storage Gen2 (Raw/Bronze container)

Enabled metadata-driven ingestion for scalability

Design Considerations

Schema drift handling

Re-runnable pipeline logic

Folder-based partitioning strategy

⚪ Step 2: Data Cleansing (Bronze → Silver Layer)

Implemented transformation logic using Azure Data Factory Mapping Data Flows:

Removed duplicate records

Handled nulls and missing attributes

Applied consistent schema and data type conversions

Standardized column naming conventions

Generated optimized Parquet/Delta outputs

Silver layer acts as the trusted, validated data zone.

🟡 Step 3: Data Transformation (Silver → Gold Layer)

This layer applies business logic and prepares dimensional models.

Key Implementations:

SCD Type 1 (Overwrite logic for non-historical changes)

SCD Type 2 (History tracking with effective & expiry dates)

Surrogate key generation

Fact and dimension table modeling

Final curated data is loaded into:

➡ Azure SQL Database

Designed for:

Optimized query performance

BI consumption

Structured relational analytics

🔁 Pipeline Orchestration

Three modular pipelines were developed:

Local → Bronze

Bronze → Silver

Silver → Gold

Features include:

Parameterized datasets

Pipeline triggers (scheduled execution)

Dependency chaining

Failure handling & monitoring

Secure secret management via Azure Key Vault

📊 Data Visualization (Power BI)

Connected Power BI to Azure SQL Database

Designed business KPIs for:

Customer analysis

Loan performance

Transaction insights

Published dashboards to Microsoft Fabric Workspace

⚙️ Key Engineering Highlights

✔ Medallion architecture implementation

✔ Dynamic and reusable ADF pipelines

✔ Secure credential management using Azure Key Vault

✔ Incremental load ready design

✔ Optimized storage format (Parquet/Delta)

✔ Modular and scalable framework

🛠 Technology Stack

Azure Data Factory

Azure Data Lake Storage Gen2

Azure SQL Database

Azure Key Vault

Power BI

Delta / Parquet format

💡 What This Project Demonstrates

As an Azure Data Engineer with 4+ years of experience, this project reflects:

Strong understanding of cloud-native data architecture

Experience building enterprise ETL frameworks

Hands-on implementation of SCD logic

Data modeling and BI integration capabilities

Production-grade orchestration and security practices
