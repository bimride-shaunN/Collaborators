# Timesheet – Python Skill: Automating Excel Reports for Business Analytics

## 📘 Task: Python-Based Excel Reporting Automation  
**Skill Focus:** Using Python (Pandas + OpenPyXL or XlsxWriter) to automate report generation and data cleanup  
**Goal:** Eliminate manual Excel work by building scripts that process raw data, create pivot tables, apply formatting, and export polished Excel files.

---

## 🧠 Why This Skill Matters

Many businesses still rely heavily on Excel for daily reporting. Automating these reports using Python:
- Saves time and reduces human error  
- Standardizes formatting and logic  
- Makes it easier to scale reporting to multiple departments or regions  
- Allows integration with APIs or databases for real-time reporting

---

## 🔍 Research & Learning Process

- Watched YouTube tutorials and read articles on:
  - Reading and writing Excel files with Pandas and OpenPyXL
  - Styling Excel sheets using XlsxWriter
  - Automating pivot table creation and chart insertion
- Explored GitHub repositories and Jupyter Notebooks that demonstrated:
  - Monthly sales report automation
  - Inventory reconciliation
  - Financial summaries

---

## ✍️ Practice Implementation

- Used a mock sales dataset with columns: Date, Product, Region, Units Sold, Revenue
- Wrote a Python script to:
  - Load raw CSV file using `pandas.read_csv()`
  - Clean and aggregate data using `groupby()` and `pivot_table()`
  - Format output (e.g., bold headers, currency formatting)
  - Export to Excel with multiple sheets (e.g., summary, raw data)

### Sample Code:
```python
import pandas as pd
import openpyxl

# Load raw data
df = pd.read_csv('sales_data.csv')

# Clean and summarize
monthly_summary = df.groupby(['Region', 'Product']).agg({'Revenue': 'sum'}).reset_index()

# Export to Excel
with pd.ExcelWriter('Monthly_Report.xlsx', engine='openpyxl') as writer:
    df.to_excel(writer, sheet_name='Raw Data', index=False)
    monthly_summary.to_excel(writer, sheet_name='Summary', index=False)
