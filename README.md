Project Structure

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
macOS / Linux python3 -m venv venv source venv/bin/activate
Windows (PowerShell) python -m venv venv .\venv\Scripts\activate
Install dbt (Snowflake adapter)
pip install dbt-snowflake
Configure profiles.yml
Edit your ~/.dbt/profiles.yml with your Snowflake credentials and ensure the profile name matches dbt_project.yml.

Running the Project
dbt debug – validate configuration and warehouse connection dbt run – execute all models dbt test – run schema and data tests dbt snapshot – build or update snapshots dbt build – full pipeline (models + tests + snapshots)

Documentation
Generate documentation: dbt docs generate
View documentation locally: dbt docs serve
This opens an interactive site with lineage graphs, model descriptions, tests, and snapshots.

Notes
This project follows dbt best practices including staging/core/marts layering, tests, macros, documentation blocks, contracts, hooks, and snapshots. Snowflake is used as the analytics warehouse.
