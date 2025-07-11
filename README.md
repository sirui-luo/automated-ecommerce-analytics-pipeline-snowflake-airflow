### 1. Project Summary
This pipeline simulates and automates analytics on e-commerce orders. It uses:

Snowflake for data warehousing

dbt for transforming raw data into clean dimensional models (e.g., orders, customers, shipping delays)

Airflow for scheduling workflows and alerting stakeholders when orders are delayed.

### 2. System Architecture Diagram
CSV → Snowflake → dbt → Airflow (DAG + alert)

### Folder Structure
ECOMMERCE_PROJECT_TUT/
│
├── airflow_project/
│   └── dags/
│       ├── order_monitor_dag.py            # Airflow DAG to orchestrate the pipeline
│       └── utils/config/
│           ├── check_delayed_orders.py     # Python script to check for delayed orders
│           └── snowflake_config.yaml       # Snowflake connection credentials
│
├── dbt_ecommerce/                          # dbt project folder for transformations
│   ├── models/
│   ├── dbt_project.yml
│   └── profiles.yml (if local)
│
├── dummy_data_creation/                    # Scripts to simulate e-commerce order data
│
├── logs/                                   # Logs from Airflow executions
│
├── airflow_venv_39/                        # Python virtual environment for Airflow
│
├── test_import.py                          # Temporary script for testing import paths
