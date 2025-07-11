### 1. Project Summary
This pipeline simulates and automates analytics on e-commerce orders. It uses:

Snowflake for data warehousing

dbt for transforming raw data into clean dimensional models (e.g., orders, customers, shipping delays)

Airflow for scheduling workflows and alerting stakeholders when orders are delayed.

### 2. System Architecture Diagram
CSV → Snowflake → dbt → Airflow (DAG + alert)
