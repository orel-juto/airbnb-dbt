# Airbnb dbt Project

This repository contains a dbt project built as part of the **Udemy dbt course – Airbnb case study**.  
It models raw Airbnb data into cleaned dimensional and fact tables, and provides analytics-ready marts.

---

## Project Structure

```text
.
├── models/
│   ├── staging/         # Staging models close to the raw source
│   ├── core/            # dim_ / fct_ business-ready models
│   └── marts/           # BI-facing, curated tables
├── seeds/               # CSV seed files loaded into the warehouse
├── snapshots/           # Slowly changing dimension snapshots
├── macros/              # Reusable macros and custom tests
├── analyses/            # Ad-hoc / exploration queries
├── tests/               # Schema & data tests
└── dbt_project.yml

Setup
Create a virtual environment

macOS / Linux
python3 -m venv venv
source venv/bin/activate

Windows (PowerShell)
python -m venv venv
.\venv\Scripts\activate

Install dbt (Snowflake adapter)

pip install dbt-snowflake

Configure profiles.yml

Edit your ~/.dbt/profiles.yml with the correct Snowflake credentials and ensure the profile name matches the one defined in dbt_project.yml.

Running the Project

dbt debug – validate project configuration and Snowflake connection
dbt run – execute all models
dbt test – run schema and data tests
dbt snapshot – run or update snapshots
dbt build – full pipeline (models + tests + snapshots)
