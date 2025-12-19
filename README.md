# Café Sales Data Cleaning and Preparation Project

## Project Overview
This project documents the end-to-end data cleaning and preparation of a real-world café sales dataset using **Python (Pandas)** in **Google Colab**.  
The raw dataset contained significant data quality issues, including missing values, inconsistent financial calculations, incorrect data types, and unstandardized formats. These issues made the data unsuitable for reliable analysis and reporting.

The objective of this project was to transform the raw dataset into a **clean, accurate, and analysis-ready dataset** that can support business insights, reporting, and decision-making.

---

## Business Problem
Café operations rely heavily on accurate sales data to make informed decisions related to pricing, inventory management, product performance, and customer behavior.  
However, poor data quality can lead to misleading insights and ineffective business strategies.

The original dataset suffered from:
- High levels of missing data
- Incorrect and inconsistent data types
- Financial inconsistencies between quantity, unit price, and total sales
- Invalid or inconsistent transaction dates
- Unstandardized categorical values

Addressing these issues was necessary to ensure analytical reliability and business value.

---

## Dataset Description
The dataset consists of **10,000 transaction records** with the following columns:

- Transaction ID  
- Item  
- Quantity  
- Price Per Unit ($)  
- Total Spent ($)  
- Payment Method  
- Location  
- Transaction Date  

---

## Data Quality Issues Identified
Initial exploration revealed the following problems:

- Missing values across 7 of the 8 columns
- Incorrect data types affecting numerical and date computations
- Inconsistent `Total Spent` values compared to derived calculations
- Unclean and inconsistent text entries
- Missing and improperly formatted transaction dates

These issues were systematically addressed during the cleaning process.

---

## Data Cleaning Strategy and Methodology
All data cleaning tasks were performed using **Python (Pandas)** in **Google Colab**.

### Key Cleaning Actions
- Replaced missing or invalid item names (including error entries) with `"Unknown"`
- Filled missing numerical values (`Quantity`, `Price Per Unit`) using **median imputation**
- Recalculated the `Total Spent` column using the formula: 'Quantity' * 'Price Per Unit'
- - Standardized and corrected date formats, filling missing dates using median imputation
- Filled missing categorical values (`Location`, `Payment Method`) using **mode** or `"Unknown"`
- Checked for duplicate records (none were found)

This approach ensured consistency, accuracy, and preservation of transaction volume.

---

## Cleaning Impact Summary

### Missing Values Before and After Cleaning

| Column | Before Cleaning | After Cleaning |
|------|----------------|---------------|
| Item | 677 (6.77%) | 0 |
| Quantity | 479 (4.79%) | 0 |
| Price Per Unit ($) | 354 (3.54%) | 0 |
| Total Spent ($) | 330 (3.30%) | 0 |
| Payment Method | 3,178 (31.78%) | 0 |
| Location | 3,961 (39.61%) | 0 |
| Transaction Date | 460 (4.60%) | 0 |

### Overall Results
- 9,439 missing values resolved across 7 columns  
- 5 columns had corrected data types  
- 330 inconsistent financial records recalculated  
- 0 rows removed, preserving the full dataset  

---

## Assumptions
To ensure transparency and reproducibility, the following assumptions were applied:

1. Zero-priced items represent valid promotional or free transactions.
2. Missing location and payment method values were filled rather than dropped to preserve transaction volume.
3. Inconsistent totals were treated as data-entry errors and recalculated.
4. Median imputation was selected to reduce sensitivity to outliers.
5. Missing transaction dates were imputed rather than removed.

---

## Tools and Technologies
- Python  
- Pandas  
- Google Colab  
- Jupyter Notebook  

---

## Final Outcome
The cleaned dataset is accurate, consistent, and ready for analytical use.  
It can be confidently applied to:
- Exploratory data analysis
- KPI development
- Business dashboards
- Sales trend and product performance analysis

This project demonstrates a structured, business-focused approach to data cleaning with emphasis on data quality, reproducibility, and analytical reliability.

---

## Limitations
- The dataset does not include additional contextual variables such as customer demographics or inventory data.
- Some values were imputed, introducing minor estimation uncertainty.
- Seasonal effects and external business factors are not captured.
- Manual data entry errors may still exist despite cleaning efforts.

---

## Author
**Hassan Mistura Olaitan**  
Aspiring Data Analyst  
Python | Data Cleaning | Data Analysis


