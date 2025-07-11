# Timesheet – Power BI Skill: Data Modeling with Star Schema and Relationships

## 📘 Task: Mastering Data Modeling in Power BI  
**Skill Focus:** Building efficient, scalable data models using star schema principles and configuring table relationships  
**Goal:** Learn to structure Power BI models that support fast, flexible analytics with minimal redundancy and maximum performance.

---

## 🧠 Why This Skill Matters

Power BI visuals and DAX measures rely heavily on the data model. A poorly designed model leads to slow performance, incorrect aggregations, and confusing relationships. Mastering the star schema ensures:
- Accurate filtering and slicing
- Easy-to-understand model logic
- Better performance, especially with large datasets

---

## 🔍 Research & Learning Process

- Watched Power BI YouTube tutorials focusing on:
  - Star schema vs. snowflake schema
  - Fact tables vs. dimension tables
  - Filter direction and cardinality (1:Many, Many:1, Many:Many)
  - Handling inactive relationships and bidirectional filters
- Read articles and guides from:
  - SQLBI.com
  - Power BI Docs: "Best Practices for Data Modeling"
  - DAX.Guide and Power BI community threads

---

## ✍️ Practice Implementation

- Created a sales analytics project with:
  - A **fact table**: Sales transactions  
  - **Dimension tables**: Dates, Customers, Products, Regions

### Key Tasks:
- Established relationships: 1-to-Many from dimensions to fact table
- Used **Date table** with `MARK AS DATE TABLE` to support time intelligence
- Avoided circular relationships and reduced unnecessary bi-directional filters
- Visualized model using **Model View** and added descriptions to fields

### Example:

---

## ⚠️ Challenges Faced

- Managing filter context with many-to-many relationships  
- Resolving ambiguous paths between tables  
- Ensuring model remains clean without redundant joins  
- Avoiding bi-directional filters unless absolutely necessary

---

## 📂 GitHub Upload Plan

- Folder: `/powerbi/data-modeling-star-schema/`
- Files:
  - `.pbix` file with full data model and relationships
  - `model_diagram.png` – screenshot of relationship view
  - `mock_data/` folder with CSVs: Sales, Products, Dates, Customers
  - `data_modeling_notes.md` – explanations, do’s and don’ts

---

## ✅ Outcome

- Learned how to build clean, high-performing Power BI models using star schema  
- Gained experience handling real-world data relationships  
- Improved understanding of filter flow and data context in visualizations  
- Created a reusable template to apply in future dashboards and reports
