# Timesheet – Tableau Skill: Level of Detail (LOD) Expressions

## 📘 Task: Advanced Tableau Concept – LOD Expressions  
**Skill Focus:** Creating and applying Level of Detail calculations in Tableau for advanced aggregation control  
**Goal:** Understand, research, and apply FIXED, INCLUDE, and EXCLUDE LOD expressions to control data granularity and enable complex comparisons.

---

## 🧠 Why This Skill Matters

Standard Tableau aggregations operate at the view level, but many business questions require controlling the level at which data is calculated—independent of what’s shown in the chart. LOD expressions allow analysts to answer those questions with precision.

Example use cases:
- Calculating average sales per customer, regardless of the number of orders  
- Comparing a region's sales to the total company average  
- Finding customer lifetime value (CLV) across years

---

## 🔍 Research & Learning Process

- Watched expert-level YouTube tutorials explaining:
  - Difference between FIXED, INCLUDE, and EXCLUDE LODs
  - Syntax, logic, and real-world use cases
  - How LODs interact with filters and dimensions in the view

- Read advanced documentation from:
  - Tableau Help Guide on LODs
  - Zen Master blogs and Medium articles
  - Tableau Community Forums (to understand common mistakes and performance tips)

---

## ✍️ Practice Implementation

Used the Superstore dataset to create and apply LOD expressions like:

### Example 1: Average Sales Per Customer
```tableau
{ FIXED [Customer Name] : SUM([Sales]) }
