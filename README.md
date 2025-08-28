# OpenFDAAPI-Azure-Antibody-RWE-MLClustering

[![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python&logoColor=white)](https://www.python.org/)
[![Azure](https://img.shields.io/badge/Azure-Cloud-0078D4?logo=microsoft-azure&logoColor=white)](https://azure.microsoft.com/)

This repository demonstrates the integration of the OpenFDA API with Azure services to process and analyze antibody-related Real-World Evidence (RWE) data. It provides a full pipeline from data ingestion to machine learning model deployment.

![Banner](banner.png)

---

## 🧱 Architecture Overview

The system architecture facilitates seamless data flow from raw ingestion to actionable insights:

- **Data Ingestion**: Azure Blob Storage collects raw data from the OpenFDA API.
- **Data Processing Layers**:
  - **Bronze Layer**: Raw, unprocessed Parquet files.
  - **Silver Layer**: Cleaned and transformed data.
  - **Gold Layer**: Aggregated and enriched data ready for ML modeling.
- **Machine Learning**: Training of clustering models using Gold Layer data.
- **Deployment Pipelines**: Automated workflows defined in JSON pipeline templates.

<details>
<summary>Architecture Diagram</summary>

![Architecture Diagram](https://learn.microsoft.com/en-us/azure/architecture/ai-ml/guide/azure-openai-gateway-multi-backend)

</details>

---

## 🧪 Data Science Workflow

The workflow follows these main steps:

<details>
<summary>Click to expand</summary>

1. **Data Collection**: Fetches adverse event data from the OpenFDA API.
2. **Data Transformation**:
   - [ParquetToCSV.ipynb](https://github.com/camontefusco/OpenFDAAPI-Azure-Antibody-RWE-MLClustering/blob/notebooks/ParquetToCSV.ipynb): Convert Parquet to CSV.
   - [Notebook1BronzeNewtoSilverProcessing.ipynb](https://github.com/camontefusco/OpenFDAAPI-Azure-Antibody-RWE-MLClustering/blob/notebooks/Notebook1BronzeNewtoSilverProcessing.ipynb): Bronze → Silver processing.
   - [PrepareGoldForML.ipynb](https://github.com/camontefusco/OpenFDAAPI-Azure-Antibody-RWE-MLClustering/blob/notebooks/PrepareGoldForML.ipynb): Prepare Gold layer for ML.
   - [ProcessGoldToCurated.ipynb](https://github.com/camontefusco/OpenFDAAPI-Azure-Antibody-RWE-MLClustering/blob/notebooks/ProcessGoldToCurated.ipynb): Curate Gold layer.
3. **Model Training**:
   - [TrainGoldMLModel.ipynb](https://github.com/camontefusco/OpenFDAAPI-Azure-Antibody-RWE-MLClustering/blob/notebooks/TrainGoldMLModel.ipynb): Clustering model training.
4. **Evaluation & Deployment**: Model validation and deployment pipelines.

</details>

---

## 🛠️ Technologies & Skills

- **Languages**: Python  
- **Data Processing**: Azure Blob Storage, Azure DataLake Gen2, Azure Synapse Analytics, Parquet, Pandas  
- **Machine Learning**: Scikit-learn, K-means Clustering  
- **Deployment**: Azure Pipelines  
- **Visualization**: Matplotlib, Seaborn  

---

## 📸 Visual Documentation

<details>
<summary>Click to expand screenshots</summary>

- **Blob to Bronze**: ![Blob to Bronze](https://github.com/camontefusco/OpenFDAAPI-Azure-Antibody-RWE-MLClustering/blob/screenshots/Blob%20to%20Bronze.png)
- **Silver to Gold**: ![Silver to Gold](https://github.com/camontefusco/OpenFDAAPI-Azure-Antibody-RWE-MLClustering/blob/screenshots/Silver%20to%20Gold.png)
- **Daily Processing**: ![Daily Processing](https://github.com/camontefusco/OpenFDAAPI-Azure-Antibody-RWE-MLClustering/blob/screenshots/Daily_processing.png)

</details>

---

## 🔗 Pipelines

<details>
<summary>Click to expand JSON pipelines</summary>

- [BlobtoBronze.json](https://github.com/camontefusco/OpenFDAAPI-Azure-Antibody-RWE-MLClustering/blob/pipelines-(json)/BlobtoBronze.json)  
- [SilverToGold.json](https://github.com/camontefusco/OpenFDAAPI-Azure-Antibody-RWE-MLClustering/blob/pipelines-(json)/SilverToGold.json)  
- [Daily_processing.json](https://github.com/camontefusco/OpenFDAAPI-Azure-Antibody-RWE-MLClustering/blob/pipelines-(json)/daily_processing.json)  

</details>

---

## 📬 Contact
Carlos Montefusco
📧 cmontefusco@gmail.com
🔗 GitHub: /camontefusco
