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
1. Create and activate a virtual environment

macOS / Linux

python3 -m venv venv
source venv/bin/activate


Windows (PowerShell)

python -m venv venv
.\venv\Scripts\activate

2. Install dbt (Snowflake adapter)
pip install dbt-snowflake

3. Configure your profiles.yml

Create or update ~/.dbt/profiles.yml with your Snowflake connection details, ensuring the profile name matches the one in dbt_project.yml.

Useful Commands
dbt debug        # Check connection and configuration
dbt run          # Run all models
dbt test         # Run tests
dbt snapshot     # Run snapshots
dbt build        # Full pipeline (models + tests + snapshots)

Documentation

Generate and view dbt documentation:

dbt docs generate
dbt docs serve


This opens an interactive UI showing:

Model and column documentation

Lineage graph

Tests, seeds, snapshots, and exposures

Notes

This project is based on the Airbnb dbt case study, modeling raw Airbnb data into staging, core, and mart layers.

Folder structure, tests, macros, contracts, and documentation follow standard dbt best practices.

Snowflake is used as the analytics warehouse.
