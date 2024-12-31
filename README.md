# Project1_QD_2024
This is a on-going Quest Diagnostics work project based on real world healthcare data of United States from 2016-2020. This project show case my ability to sue SQL for data processing and exploratory data analysis, building timely refresh data pipeline for autorefresh and reflect the data insight using Amazon Quick Sight (AWS) dashboard.

## Future Task:
Prediction model is in preductive and the prediction model will be able to be reflected on the interactive dashboard for clients' need.

## Key Features:
- Interactive dashboard built using AWS Quick Sight.
- Insights of Diabetes trends in United States population from State level to Zipcode.
- Code for data preparation and cleaning in SQL
- Data pipeline built using Matallion ETL

## Preview
### Dashboard Overview

### Key Insight

## Files

- `code/`: SQL scripts and Jupyter Notebook for data cleaning and preparation.
- `databoard/`: Quick sight file for the interactive dashboard.
- `pipeline/`: Matallion ETL pipeline for data timely, autorefresh.

## Usage:
1. Download the repository
2. Open Diabetes_MY.xxx in Quicksight Reader or preview with the screenshot.
3. Explore the interactive dashboard.

## About the Dataset:
This dataset contains healthcare lab results and demographic information from 2016-2024, with the following fields:
- `ACCN_ID`: Accession ID
- `LOINC`: Loinc Code
- `ORDER_NAME`
- `RESULT_NAME`
- `RESULT_VALUE`

## Tools Used:
- **Snowflake** - Data preparation for SQL
- **Matallion** - Data pipeline
- **Amazon Quicksight** - Dashboard building

## Project sturcture
### 1. Data cleaning
   - Keep only rows with valid Patient ID and in date range 2016 to present date.
   - Research through lab test options keep only the test result that is related to diabetes and prediabetes diagnostics.
   - Filter the data use `LOINC_CODE` that match the test that is needed for analysis, and normalize the `LOINC_CODE`.
   - Normalization `RESULT_VALUE` by getting rid of unrelated string, sign and unrealistic number that is out of range.
   - Categorize each patient record based on the `RESULT_VALUE` to 'Diabetes', 'Prediabetes' and 'Normal'.
### 2. Data manipulation
   - Converting to different data types.
   - Creating new features that could be directly used in dashboard.
   - Merge lab data file with diagnostic infornation file and third party data file.
### 3. Data Preparation and qulity check
   - Make sure every result is proper Normalized
   - Make sure we didn't accidently loose valueable data while cleaning.
   - Make sure NULL values are treated correctly.
   - Compare outcome percentage with general data for difference.
### 4. Data Pipeline
   - Seperate last 30 days data from the original (last updated) cleaned data tabel.
   - Merge two data file by
### 5. Data Visualization
   - Set up calculation field

