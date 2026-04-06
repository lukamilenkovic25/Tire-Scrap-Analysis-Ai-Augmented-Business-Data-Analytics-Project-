# Tire-Scrap-Analysis-Ai-Augmented-Business-Data-Analytics-Project-

## 1. Project Overview

This project provides a complete end‑to‑end analysis of tire scrap data using a modern, AI‑augmented analytical workflow.  
The goal is to demonstrate capabilities relevant for **Business Analyst** and **Data Analyst** roles, including:

- Data cleaning & quality control (Excel)
- Data modeling with DAX (Power BI)
- Business‑oriented KPI development
- AI‑driven insight generation (Key Influencers, Decomposition Tree, Anomaly Detection)
- Clear visual storytelling across two dashboard pages

The dataset represents monthly scrap output per production line, machine, shift and root cause.

---

## 2. Tools & Technologies
- **Excel** – data cleaning, preprocessing  
- **Power BI** – modeling, DAX measures, dashboard creation  
- **Power BI AI Visuals** – Key Influencers, Decomposition Tree, Anomaly Detection  
- **Generative AI** – used for analytical reasoning, hypothesis validation, and summary creation  

---

## 3. Dataset
**Dataset size:** 500 records  
**Columns included:**
- Date  
- Production Line  
- Machine  
- Shift  
- Scrap (KG)  
- Scrap Cost (€)  
- Cause of scrap  

Data was intentionally “dirty” to simulate a real manufacturing environment  
(invalid dates, inconsistent naming, text‑formatted numbers, missing values).

---

## 4. Data Model (Power BI)
### Calculated Columns
MonthName = FORMAT('ScrapData'[Date], "MMM")
MonthNumber = MONTH('ScrapData'[Date])

### Measures
Total Scrap KG = SUM('ScrapData'[Scrap_KG])
Total Scrap Cost = SUM('ScrapData'[Scrap_Cost_EUR])
Avg Scrap per Day = AVERAGEX(VALUES('ScrapData'[Date]), CALCULATE([Total Scrap KG]))
Scrap Cost per KG = DIVIDE([Total Scrap Cost], [Total Scrap KG])

---
