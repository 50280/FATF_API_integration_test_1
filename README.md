## Description of underlying logic & structure


## Description of who to contact for maintenance 


## Link to documentation & maintenance guide


## Repository Strcuture Description

repo-root/
├─ 00_infrastructure/
│  ├─ 01_docker/                 # local setup, containers, etc.
│  └─ 02_migrations/             # database DDLs or schema migrations
│
├─ 01_extract/                   # extraction layer (API + legacy)
│  ├─ 01_legacy_data/            # scripts to ingest historical data
│  └─ 02_API/                    # API extraction logic
│
├─ 02_clean/                     # cleaning and standardization
│  ├─ 01_rules/                  # mapping or cleaning rules
│  ├─ 02_transforms/             # transformation scripts (Python/SQL)
│  └─ 03_merge/                  # intermediate joins or merge logic
│
├─ 03_merge/                     # merging stage (integration)
│  ├─ 01_SQL/                    # SQL merge scripts
│  ├─ 02_models/                 # models or intermediate tables
│  └─ 03_tests/                  # merge-level validation tests
│
├─ 04_publish/                   # publishing or output stage
│  └─ (empty or WIP)             # final outputs / exports / marts
│
├─ 04_reports_powerBI/           # Power BI reporting artifacts
│  ├─ 01_JAT/                    # report set A
│  ├─ 02_learningB/              # report set B
│  ├─ 03_learningC/              # report set C
│  └─ 04_learningD/              # report set D
│
└─ README.md                     # (recommended) overview of repo
