%md
# Analisis_Precios_Medicamentos - README

## Overview

This repository contains the Databricks notebook `Analisis_Precios_Medicamentos`, which analyzes medication prices in Argentina. The analysis uses the provided CSV file and builds a multi-layered data pipeline (Bronze, Silver, Gold) with Delta tables. The final results are visualized in an interactive Databricks Dashboard.

## Prerequisites

- Access to Databricks on AWS
- A running Databricks cluster (attach the notebook to your cluster)
- The CSV file: `Precios_Medicamentos.csv` (included in this repo)

## How to Run

1. **Upload the CSV file**  
   Upload `Precios_Medicamentos.csv` to your Databricks workspace or a Unity Catalog volume.

2. **Import the Notebook**  
   Import `Analisis_Precios_Medicamentos` notebook into your Databricks workspace.

3. **Attach to Cluster**  
   Attach the notebook to your Databricks cluster.

4. **Run All Cells**  
   Run all cells in the notebook sequentially. The notebook will:
   - Read and clean the CSV data
   - Create Delta tables for each layer (Bronze, Silver, Gold)
   - Enrich the data with currency conversion from an external API
   - Calculate new metrics and build the final Gold table

5. **View the Dashboard**  
   The notebook includes a Databricks Dashboard that visualizes key metrics and trends from the analysis.  
   - To access the dashboard, click the Dashboard icon in the notebook toolbar.
   - The dashboard provides interactive charts and tables for exploring medication prices, coverage, and currency conversion.

<img width="1914" height="889" alt="Dashboard_Databricks" src="https://github.com/user-attachments/assets/7e08f50b-7706-47cc-ab01-e04a07865e8b" />


## Notes

- All code is written in Python using PySpark DataFrames.
- The pipeline is modular and can be extended for additional data sources or metrics.
- The dashboard is fully interactive and can be customized for further insights.

---
For any issues or questions, please open an issue in this repository.
