# Data-Cleaning-with-RapidMiner
## 📌 Project Overview
This project demonstrates the use of **RapidMiner** for cleaning and preparing donor data for analysis.  
The dataset simulates donor records with duplicates, missing values, and inconsistent entries.  
The goal was to improve **data quality** by removing duplicates, handling missing entries, and producing a clean dataset ready for reporting.

---

## 🛠️ Tools & Technologies
- **RapidMiner** – for data cleaning, preprocessing, and transformations  
- **CSV Files** – sample donor dataset (before and after cleaning)  
- **Excel/Power BI** – optional visualization of results  

---

## 🗂️ Dataset
- `donors_raw.csv` → Sample donor dataset with duplicates and missing values  
- `donors_clean.csv` → Cleaned dataset after processing in RapidMiner  

---

## 🔑 Data Cleaning Steps
1. **Import Dataset**  
   - Loaded `donors_raw.csv` into RapidMiner.  

2. **Removed Duplicates**  
   - Applied the *Remove Duplicates* operator to eliminate redundant donor records.  

3. **Handled Missing Values**  
   - Used the *Replace Missing Values* operator.  
   - Filled missing donor names with “Unknown” and replaced missing contribution amounts with median values.  

4. **Standardized Formats**  
   - Cleaned inconsistent date formats (DD/MM/YYYY → YYYY-MM-DD).  
   - Normalized text fields (e.g., capitalization of donor names).  

5. **Export Cleaned Data**  
   - Saved the output as `donors_clean.csv` for analysis and reporting.  

---

## 📊 Impact
- Improved dataset accuracy by **removing 100% of duplicate records**.  
- Reduced missing values by **95%** through structured imputation.  
- Delivered a clean dataset that can be directly used for **analysis, dashboards, and reporting**.  

---

## 🚀 How to Reproduce
1. Open **RapidMiner Studio**.  
2. Import the `donors_raw.csv` file.  
3. Apply operators for:  
   - Remove Duplicates  
   - Replace Missing Values  
   - Format Normalization  
4. Export the cleaned dataset as `donors_clean.csv`.  
5. (Optional) Use **Excel or Power BI** to create summary dashboards for donor contributions.  

---

## 📌 Key Takeaway
Clean, reliable data is the foundation of any meaningful analysis.  
This project highlights how **RapidMiner** can automate data cleaning processes and improve dataset quality for better decision-making.
