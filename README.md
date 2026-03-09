# Earthquake Data Pipeline (Azure Databricks)

This project implements a **Bronze-Silver-Gold data pipeline** using Azure Databricks and PySpark to process earthquake data from the USGS API.

## Architecture

The pipeline follows the Medallion Architecture:

Bronze → Raw data ingestion  
Silver → Cleaned and structured data  
Gold → Enriched analytics dataset

## Technologies Used

- Azure Databricks
- PySpark
- Azure Data Lake Storage (ADLS)
- Databricks Workflows
- Python
- Reverse Geocoding

## Pipeline Stages

### Bronze Layer
- Retrieves earthquake data from the **USGS Earthquake API**
- Stores raw JSON data in Azure Data Lake
- Orchestrated using Databricks Workflows

Notebook:

### Silver Layer
- Loads raw JSON data
- Cleans and structures the dataset
- Converts timestamps
- Stores processed data in **Parquet format**

Notebook:

### Gold Layer
- Enriches data using reverse geocoding
- Adds country and significance classification
- Produces analytics-ready dataset

Notebook:

## Workflow Orchestration

The pipeline is automated using **Databricks Jobs & Workflows**:

Bronze Task → Silver Task → Gold Task

Each stage passes parameters to the next task using:

## Example Data Flow

USGS API  
↓  
Bronze (Raw JSON)  
↓  
Silver (Clean Parquet Data)  
↓  
Gold (Enriched Analytics Dataset)

## Architecture
<img width="761" height="220" alt="image" src="https://github.com/user-attachments/assets/379638de-6dda-4e23-96c0-6b374508bbe4" />


## Author

Jamil Al-rubaye  
Automation Engineering Student  
Oulu University of Applied Sciences
