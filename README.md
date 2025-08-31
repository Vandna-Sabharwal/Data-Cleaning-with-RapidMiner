# Data Cleaning with RapidMiner

## Project Overview
This project demonstrates the use of **RapidMiner** and **Python** for cleaning and preparing donor data for analysis.  
The dataset includes duplicates, missing values, and inconsistent date formats.  
The goal is to improve **data accuracy** and make the dataset ready for reporting and dashboards.  

## Tools & Technologies
- **RapidMiner** – for data cleaning workflows  
- **Python (Pandas)** – for additional checks and validation  
- **Excel / Power BI** – for visualization  

## Data Cleaning Steps
1. Imported raw donor dataset (`donors_raw.csv`) into RapidMiner.  
2. Removed duplicates using *Remove Duplicates* operator.  
3. Replaced missing values with placeholders or median values.  
4. Standardized inconsistent date formats.  
5. Exported cleaned dataset (`donors_clean.csv`).  
6. Validated results in Python.  

## Validate via Python
import pandas as pd

# Load raw and cleaned datasets
raw = pd.read_csv("donors_raw.csv")
clean = pd.read_csv("donors_clean.csv")

# Check duplicates in raw data
print("Raw duplicates:", raw.duplicated().sum())

# Check missing values before cleaning
print("Raw missing values:\n", raw.isnull().sum())

# Confirm cleaned dataset integrity
print("Clean duplicates:", clean.duplicated().sum())
print("Clean missing values:\n", clean.isnull().sum())
