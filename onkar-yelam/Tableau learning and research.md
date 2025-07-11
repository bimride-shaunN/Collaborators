from pathlib import Path

# Markdown content for Tableau learning and research documentation
tableau_learning_md = """
# Timesheet – Tableau Learning and Research Documentation

## 📘 Task: Tableau Skill Development  
**Objective:** Learn to use Tableau for data visualization and storytelling by following structured tutorials and independent research. Focused on creating dashboards, exploring chart types, and applying business context to visual insights.

---

## 🎥 YouTube Learning Process

- Watched beginner to intermediate YouTube playlists covering:
  - Tableau Desktop interface walkthrough
  - Connecting to Excel, CSV, and sample data sources
  - Creating bar charts, line graphs, maps, tables, and KPIs
  - Using filters, parameters, and calculated fields
  - Building interactive dashboards with multiple views and navigation
- Followed along in Tableau Public using Superstore dataset and other mock business datasets

---

## 🔍 Research & Reading

- Explored Tableau Public Gallery for inspiration and layout techniques
- Read blog articles and guides from:
  - Tableau official site
  - Data visualization best practice blogs
  - Medium and Reddit threads on optimizing dashboards and performance
- Learned about:
  - Dimensions vs. Measures
  - Discrete vs. Continuous fields
  - Dashboard design principles (e.g., Z-pattern layout, white space, color use)
  - Publishing to Tableau Public and Tableau Server

---

## 🧰 Concepts & Tools Covered

- Filters, sets, groups, and hierarchies  
- Dual-axis charts and combination views  
- Table calculations and LOD (Level of Detail) expressions  
- Actions: filter actions, highlight actions, URL actions  
- Interactive elements like drop-down selectors and dynamic titles  
- Exporting dashboards and embedding visualizations  

---

## ✅ Outcome

- Developed foundational Tableau skills for data exploration and dashboard storytelling  
- Built practice dashboards using retail, sales, and customer datasets  
- Gained confidence in using Tableau Public for real-time visualization work  
- Ready to apply Tableau to business reporting, stakeholder presentations, and analytics projects
"""

# Save the file
file_path = Path("/mnt/data/tableau_learning_research.md")
file_path.write_text(tableau_learning_md)

file_path.name
