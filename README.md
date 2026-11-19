# Customer Churn — Data Quality and Exploratory Analysis

## Project overview
This project audits and explores the supplied customer churn sample for Internship Task 02.

## Dataset
- 15 rows and 11 columns
- Supplied customer sample pasted from the provided EdVyro CSV resource
- The raw input is preserved as `customer_churn_raw.csv`

## Files
- `customer_churn_analysis.ipynb` — reproducible end-to-end Python notebook
- `customer_churn_raw.csv` — original supplied records
- `cleaned_customer_churn.csv` — cleaned export (standardized snake_case headers)
- `data_quality_report.pdf` — findings, quality decisions, charts and limitations
- `data_dictionary.csv` — field definitions and checks
- `missing_value_audit.csv` — missing-value counts
- `iqr_outlier_audit.csv` — IQR screening results
- `numeric_summary_statistics.csv` — descriptive statistics
- `charts/` — exported exploratory charts

## Run
Install dependencies:
```bash
pip install pandas numpy matplotlib jupyter
```
Open `customer_churn_analysis.ipynb` in Jupyter Notebook / JupyterLab and run all cells from this folder.

## Key results
- 15 records; no missing cells; no exact duplicate rows
- 7 churned / 8 not churned; sample churn rate 46.7%
- No IQR-flagged outliers across the five numeric fields
- All total-charge values match monthly charges × tenure months within 0.01
- All 7 Month-to-Month records are marked churned in this sample; none of the longer-contract records are marked churned
- Churned customers average 4.29 support tickets versus 1.00 for non-churned customers

## Important limitations
This is a very small sample (15 records). Treat all findings as descriptive observations only. Do not infer causation or generalize these rates to a real customer population. Currency and churn observation window were not specified in the supplied data.
