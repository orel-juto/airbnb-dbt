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
Create and activate a virtual environment

macOS / Linux:

bash
Copy code
python3 -m venv venv
source venv/bin/activate
Windows (PowerShell):

powershell
Copy code
python -m venv venv
.\venv\Scripts\activate
Install dbt (Snowflake adapter)

bash
Copy code
pip install dbt-snowflake
Configure profiles.yml

Create or update your profiles.yml (usually under ~/.dbt/) with your Snowflake credentials and a profile that matches dbt_project.yml (profile name, target, schema, etc.).

Common Commands
From the project root:

bash
Copy code
# Check connection and configuration
dbt debug

# Run all models
dbt run

# Run tests (schema + data tests)
dbt test

# Run snapshots
dbt snapshot

# Full pipeline (models + tests + snapshots)
dbt build
Documentation
Generate and view the dbt documentation site:

bash
Copy code
dbt docs generate
dbt docs serve
This will open an interactive UI with:

Model documentation and column descriptions

Lineage graph

Tests and exposures
