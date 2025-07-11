# Timesheet – Power BI Skill: Time Intelligence with DAX Measures

## 📘 Task: Mastering DAX for Time-Based Calculations  
**Skill Focus:** Using DAX time intelligence functions to perform date-based comparisons and historical analysis  
**Goal:** Understand how to write complex DAX expressions to analyze trends across months, quarters, and years, enabling better business decision-making.

---

## 🧠 Why This Skill Matters

Most businesses need to track performance over time—whether it’s revenue growth, user engagement, or churn rates. Time intelligence in DAX allows you to:
- Compare current period vs. previous period
- Calculate running totals
- Perform YoY, MoM, QTD, YTD comparisons
- Handle custom fiscal calendars

These analyses aren't possible with standard aggregations and require advanced DAX logic.

---

## 🔍 Research & Learning Process

- Watched advanced Power BI tutorials on YouTube focused on:
  - CALCULATE, DATEADD, SAMEPERIODLASTYEAR, TOTALYTD
  - Handling filter context and dynamic date ranges
- Read expert blogs and documentation from:
  - SQLBI.com (Marco Russo & Alberto Ferrari)
  - Microsoft Learn: Time Intelligence in Power BI
  - Community forums and DAX Pattern Libraries
- Studied behavior of DAX in context of slicers, visuals, and relationships

---

## ✍️ Practice Implementation

Used a sales dataset to build a dashboard that included:
- Year-over-Year sales comparisons
- Month-over-Month customer growth
- Cumulative revenue charts

### Example DAX Measures:
```DAX
Sales LY = CALCULATE(SUM(Sales[Amount]), SAMEPERIODLASTYEAR(Dates[Date]))

MoM Growth % = 
VAR CurrentMonth = CALCULATE(SUM(Sales[Amount]))
VAR PrevMonth = CALCULATE(SUM(Sales[Amount]), DATEADD(Dates[Date], -1, MONTH))
RETURN DIVIDE(CurrentMonth - PrevMonth, PrevMonth)
