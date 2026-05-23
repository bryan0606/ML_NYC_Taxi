# NYC Yellow Taxi Trip Records — Big Data Analysis

## 📋 Project Overview

This project performs large-scale data management and machine learning on the NYC Yellow Taxi Trip Records (January 2024) dataset using Apache Spark on Databricks Community Edition. The notebook covers:

* Data ingestion and cleaning with SparkSQL and Spark DataFrames
* Exploratory Data Analysis (EDA)
* Feature engineering and correlation analysis
* Machine learning model training (Linear Regression and Random Forest) using SparkML
* Hyperparameter tuning and model evaluation
* Operational efficiency modelling

## 🛠️ Prerequisites

Before running the notebook, ensure you have the following:

Databricks Community Edition Free account at [community.cloud.databricks.com](https://community.cloud.databricks.com)|

## 📦 Dataset

* Data source: https://www.kaggle.com/datasets/ibrahimqasimi/nyc-yellow-taxi-trip-records-january-2024
* Format: CSV
* Size: ~2.8 million trip records

## 🚀 Setup & Execution Instructions

### Step 1 — Create a Databricks Community Edition Account

1. Visit [https://community.cloud.databricks.com](https://community.cloud.databricks.com).
2. Sign up for a free account (or log in if you already have one).

### Step 2 — Upload the Dataset

1. From the sidebar, click + New → Add or upload Data → Create or modify table → Upload File.
2. Upload the dataset file: `nyc_tlc_yellow_2024_01.csv`.
3. Note the DBFS path after upload — it will typically be in the format of [Catalog].[Schema].[Table name]. The path used in this case is largedata.default.nyc\_tlc\_yellow\_2024\_01
4. Update the file path variable in Section 1 (Data Ingestion) of the notebook if it differs.

### Step 3 — Import the Notebook

1. From the sidebar, click Workspace → your username folder.
2. Click the dropdown arrow → Import.
3. Select File and upload `NYC_Yellow_Taxi_Trip_Records.ipynb`.
4. The notebook will appear in your workspace.

### Step 4 — Run the Notebook

1. Open the imported notebook.

Run cells sequentially from top to bottom. Each section builds on the previous one — do not skip sections.

|**Section 1**|Data Ingestion & Cleaning — loads the file, handles nulls, removes outliers|
|**Section 2**|Exploratory Data Analysis (EDA) — distributions, vendor stats, location counts, correlations|
|**Section 3**|Feature Engineering — derives `pickuphour`, `tripdurationmin`, `speedmph`, `isweekend`, etc.|
|**Section 4**|Machine Learning (Revenue Model) — Linear Regression vs Random Forest on `totalamount`|
|**Section 5**|Operational Efficiency Model — Random Forest predicting `revpermin`|
|**Section 6**|Hyperparameter Tuning — manual grid search for best model configurations|

To run all cells at once:

* Click Run All in the top toolbar

## ⚙️ Key Configuration Variables

At the start of the notebook, verify/update the following variables:

# Section 1 — Data path
df = spark.table("my_catalog.default.nyc_tlc_yellow_2024_01")

📊 Expected Outputs

After a full run, the notebook will produce:

\* EDA visualisations — histograms, scatter plots, heatmaps, bar charts
\* Correlation matrix for numeric features
\* Model performance metrics



