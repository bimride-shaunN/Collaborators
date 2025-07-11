from pathlib import Path

# Markdown content for Power BI learning and research documentation
powerbi_learning_md = """
# Timesheet – Power BI Learning and Research Documentation

## 📘 Task: Power BI Skill Development  
**Objective:** Learn to use Microsoft Power BI for business data analysis, visualization, and dashboard creation. Focused on practical application through video tutorials and independent research.

---

## 🎥 YouTube Learning Process

- Followed a structured beginner-to-advanced Power BI YouTube playlist covering:
  - Introduction to Power BI and its interface (Desktop, Service, Mobile)
  - Importing and transforming data using Power Query
  - Creating visualizations (bar, line, card, matrix, slicers)
  - Writing basic DAX (Data Analysis Expressions) for measures and calculated columns
  - Designing responsive, interactive dashboards with filters and drill-downs
- Practiced building dashboards in Power BI Desktop alongside tutorials
- Watched case-study-based videos (e.g., sales performance, customer feedback dashboards) to learn real-world use

---

## 🔍 Research & Supplementary Reading

- Explored Microsoft Learn documentation and Power BI Blog:
  - Understanding star schema and data modeling best practices
  - Filtering, cross-filter direction, and relationships between tables
  - Performance optimization techniques for large datasets
- Read articles and guides on:
  - Dashboard layout design and UX principles
  - Publishing reports to Power BI Service
  - Sharing dashboards and setting access roles for stakeholders

---

## 🧰 Concepts Covered

- Power Query Editor basics: merging, filtering, and cleaning data  
- DAX formulas: SUM, AVERAGE, CALCULATE, IF, DATEADD  
- Slicer usage for time filtering and category drilldown  
- Page navigation and bookmarks for interactive dashboards  
- Import vs. DirectQuery mode  
- Connecting Power BI with Excel, CSV, and SQL sources  

---

## ✅ Outcome

- Built foundational and intermediate-level knowledge of Power BI  
- Practiced hands-on dashboard creation using sample datasets  
- Understood how to apply Power BI in business use cases for reporting, tracking KPIs, and uncovering trends  
- Documented learnings and prepared for future integration of Power BI into project repositories
"""

# Save the file
file_path = Path("/mnt/data/powerbi_learning_research.md")
file_path.write_text(powerbi_learning_md)

file_path.name
