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
