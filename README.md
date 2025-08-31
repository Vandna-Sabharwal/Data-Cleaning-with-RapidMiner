import pandas as pd

# Load raw dataset
raw = pd.read_csv("donors_raw.csv")

print("---- RAW DATASET INFO ----")
print("Total Rows:", len(raw))
print("Duplicate Records:", raw.duplicated().sum())
print("Missing Values:\n", raw.isnull().sum())
print("\nSample Raw Data:\n", raw.head())

# Step 1: Remove duplicates (based on Donor_ID or full row)
clean = raw.drop_duplicates(subset=["Donor_ID"])

# Step 2: Handle missing donor names
clean["Donor_Name"] = clean["Donor_Name"].fillna("Unknown")

# Step 3: Handle missing contribution amounts (replace with median)
median_amount = clean["Contribution_Amount"].median()
clean["Contribution_Amount"] = clean["Contribution_Amount"].fillna(median_amount)

# Step 4: Standardize date format to YYYY-MM-DD
clean["Donation_Date"] = pd.to_datetime(clean["Donation_Date"], errors="coerce").dt.strftime("%Y-%m-%d")

# Save cleaned dataset
clean.to_csv("donors_clean.csv", index=False)

print("\n---- CLEANED DATASET INFO ----")
print("Total Rows:", len(clean))
print("Duplicate Records:", clean.duplicated().sum())
print("Missing Values:\n", clean.isnull().sum())
print("\nSample Clean Data:\n", clean.head())

print("\n✅ Data cleaning completed! Cleaned dataset saved as 'donors_clean.csv'")
