# Incremental CDC Pipeline for Banking Transactions

## Business Problem
Banking systems generate frequent transaction updates. Full data reloads are costly
and inefficient. This project implements an incremental CDC pipeline using SCD Type 2
to maintain historical audit trails.

## Architecture
Source → CDC Detection → Delta MERGE → Curated History Table

## Technologies Used
- PySpark
- Delta Lake
- Spark SQL
- Databricks Community Edition

## Key Features
- Incremental CDC processing
- SCD Type 2 implementation
- Delta MERGE INTO
- Time travel and rollback
- Audit-ready historical tracking

## Results
- Reduced processing cost and time
- Enabled audit and compliance analysis
- Improved data reliability





** Incremental CDC Pipeline for Banking Transactions **
- Business Use Case

Banks generate thousands of transaction updates daily. Performing full reloads is costly and inefficient.
This project implements an incremental CDC (Change Data Capture) pipeline with SCD Type 2, audit logging, and performance optimization, simulating a production-grade banking data engineering workflow.

- Tech Stack

Python & PySpark – ETL and transformations

Delta Lake – Historical SCD Type 2 storage, time-travel

Databricks Community Edition – Notebook execution & simulation of ADF pipelines

SQL – Merge queries & table operations

GitHub Actions – CI/CD simulation for pipeline validation

Documentation – Data lineage and audit tracking

- Architecture

Pipeline Steps:

Source CSV Files – Daily transaction CSVs (data/transactions_day1.csv, transactions_day2.csv)

CDC(Change Data Capture) Detection – Detect new and updated transactions

SCD Type 2 Merge – Update historical records using Delta MERGE

Data Quality Checks – Null, duplicate, and business rule validations

Audit Logging – Save audit metrics to transactions_audit_log table

Performance Optimization – Partitioning by transaction_date and ZORDER for fast analytics

Consumption – Curated tables ready for reporting or BI tools