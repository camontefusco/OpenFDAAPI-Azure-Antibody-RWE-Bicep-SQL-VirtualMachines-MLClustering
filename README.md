# OpenFDAAPI-Azure-Antibody-RWE-Bicep-SQL-VirtualMachines-MLClustering

pharma-azure-antibody-rwe/
│
├── infra/
│   ├── bicep/                    # Bicep scripts for Blob, SQL, Functions, VM
│   └── arm_templates/            # Generated ARM JSON for deployment
│
├── functions/
│   ├── ingest_antibody.py        # Function to pull raw JSON from OpenFDA
│   └── transform_to_silver.py    # Function to parse/edit raw data into clean format
│
├── vm/
│   └── clustering_script.py      # Script performing ML clustering on VM
│
├── sql/
│   └── create_gold_tables.sql    # SQL to load silver data and run aggregation
│
├── reporting/
│   └── powerbi_demo.pbix         # Demo report connected to Azure SQL
│
└── README.md                     # Full architecture diagram + setup steps
