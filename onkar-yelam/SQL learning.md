from pathlib import Path

# Markdown content for SQL learning and research documentation
sql_learning_md = """
# Timesheet – SQL Learning and Analytics Research Documentation

## 📘 Task: SQL Skill Development for Data Analytics  
**Objective:** Learn and apply SQL for querying, analyzing, and interpreting datasets with a focus on business and marketing analytics. Explored SQL functions, database structures, and performance-driven queries to support decision-making.

---

## 🎥 Learning Process

### 1. YouTube Tutorials
- Watched structured SQL tutorial series for analytics, including:
  - Basics of databases, tables, and schema
  - SELECT, WHERE, ORDER BY, GROUP BY, HAVING, LIMIT clauses
  - Aggregate functions (SUM, COUNT, AVG, MIN, MAX)
  - JOIN operations (INNER, LEFT, RIGHT, FULL)
  - Subqueries, CTEs, window functions, and CASE statements
- Followed real-time use cases using marketing, sales, and web traffic datasets.

### 2. Course & Platform Practice
- Completed beginner to intermediate exercises on:
  - LeetCode (SQL practice problems)
  - Mode Analytics SQL tutorials
  - W3Schools & Khan Academy SQL basics
- Practiced querying on sample datasets (e.g., customer orders, sessions, campaigns)
- Learned query optimization strategies and the importance of indexing and query planning

---

## 🔍 Topics Covered

- Understanding relational database structure  
- Writing clean, efficient queries  
- Filtering and segmenting user behavior by attributes  
- Calculating KPIs like conversion rate, customer lifetime value (CLV), and retention  
- Building nested queries and temporary views  
- Tracking marketing campaign performance and churn with SQL  
- Using SQL for funnel analysis and cohort segmentation  

---

## 🧰 Practical Application Plan

- Plan to connect SQL to analytics dashboards via:
  - Google BigQuery
  - PostgreSQL + Tableau/Power BI
- Design mock dashboards using SQL queries as back-end data sources
- Build SQL scripts to analyze:
  - Top-performing campaigns
  - Monthly active users
  - Retention and churn analysis
  - Session trends and behavior funnels

---

## ✅ Outcome

- Gained strong foundational and intermediate SQL skills
- Practiced analytics use cases using real-world marketing and business data
- Confident in using SQL for KPI reporting, segmentation, and trend analysis
- Documented all key concepts and hands-on learnings for future reference
"""

# Save the file
file_path = Path("/mnt/data/sql_learning_for_analytics.md")
file_path.write_text(sql_learning_md)

file_path.name
