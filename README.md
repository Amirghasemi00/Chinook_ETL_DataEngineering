# Chinook Data Engineering Pipeline

This project was developed to explore ETL pipelines and data warehousing using the Chinook database.

Two different approaches were implemented to process data from SQL Server into a data warehouse.

### 1. Airflow Pipeline

Uses Apache Airflow to schedule and manage ETL tasks. After the initial full load, incremental changes are processed using SQL Server CDC. The pipeline uses PostgreSQL for staging, ClickHouse for data warehousing, and Grafana for visualization.

### 2. Kafka Pipeline

Uses Apache Kafka to transfer database changes between a producer and consumer. Changes from SQL Server CDC are processed incrementally and applied to PostgreSQL and ClickHouse, with Grafana used for reporting.

Both versions support full and incremental loading, SCD Type 1 and Type 2, and data validation.

### Technologies

Python, Pandas, SQL Server, PostgreSQL, ClickHouse, Apache Airflow, Apache Kafka, Docker, and Grafana.
