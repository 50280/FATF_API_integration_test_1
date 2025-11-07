## Description of underlying logic & structure


## Description of who to contact for maintenance 


## Link to documentation & maintenance guide


## Repository Strcuture Description

```
repo-root/
├─ 01_preprocess_legacy_data/
│  ├─ 01_data_mapping/           # mapping old schema → new schema
│  └─ 02_data_cleaning/          # standardize + validate legacy files
│
├─ 02_integrate_API_data/        # merge API and preprocessed legacy data
│  ├─ raw/                       # API JSON/CSV dumps (optional)
│  ├─ staging/                   # combined tables before upload
│  └─ logs/                      # API call + integration logs
│
├─ 03_upload_API_to_SQL/         # push merged dataset to SQL
│  ├─ ddl/                       # create table scripts
│  ├─ dml/                       # insert/update/merge statements
│  ├─ utils/                     # helper functions for DB connections
│  └─ validation/                # row counts, schema checks, etc.
│
├─ 04_power_BI/                  # Power BI dashboards + helper code
│  ├─ 00_helper_functions/       # shared Power BI or DAX utilities
│  ├─ 01_JAT/                    # dashboard group 1
│  ├─ 02_XX/                     # dashboard group 2
│  ├─ 03_XX/                     # dashboard group 3
│  ├─ 04_XX/                     # dashboard group 4
│  └─ 05_XX/                     # dashboard group 5
│
├─ 05_other_outputs/             # misc exports / interim data
│  ├─ logs/                      # optional: run logs
│  ├─ archive/                   # old CSVs or reports
│  └─ temp/                      # temp outputs not for prod
│
├─ config/
│  ├─ connections.yml            # DB + API connection details
│  └─ params.yml                 # environment / global params
│
├─ scripts/
│  ├─ run_all.py                 # orchestrate 01→05 steps
│  ├─ upload_to_sql.py
│  └─ publish_powerbi.ps1
│
├─ tests/
│  ├─ unit/                      # unit tests for scripts
│  ├─ integration/               # integration tests (API + SQL)
│  └─ e2e/                       # end-to-end run validation
│
├─ .github/workflows/
│  ├─ ci.yml                     # linting + testing on push
│  └─ schedule.yml               # automated nightly pipeline
│
├─ .env.example
└─ README.md

```
