
# AI-Driven Business Intelligence System

An **end-to-end business intelligence platform** that automates **ETL, KPI forecasting, and anomaly detection** using **Airflow, AWS, Prophet, and Power BI**.

---

## Overview

This project builds a self-updating BI system that:
- Ingests and transforms data from multiple sources (CRM, ERP, APIs)
- Forecasts key performance indicators (revenue, churn, conversion rate) with **Prophet**
- Detects anomalies using statistical and residual methods
- Sends real-time alerts to **Slack** or **AWS SNS**
- Publishes curated data for dashboards in **Power BI**

---

## Architecture

mermaid
graph TD
A[CRM/ERP/API Data Sources] --> B[Airflow ETL Pipelines]
B --> C[S3 Raw Layer]
C --> D[AWS Glue / PySpark Transform]
D --> E[Snowflake / Postgres DW]
E --> F[Prophet Forecasting Models]
F --> G[Anomaly Detection Engine]
G --> H[Slack / AWS SNS Alerts]
E --> I[Power BI Dashboards]
