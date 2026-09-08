# 📊 Superstore Sales & Supply Chain Analytics Dashboard

![Excel](https://img.shields.io/badge/Tool-Microsoft_Excel-107C41?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![Power Query](https://img.shields.io/badge/ETL-Power_Query-F2C94C?style=for-the-badge)
![Power Pivot](https://img.shields.io/badge/Data_Model-Power_Pivot_&_DAX-0078D4?style=for-the-badge)

## 📌 Executive Summary
This project delivers an end-to-end interactive **Executive Sales & Supply Chain Dashboard** built using **Advanced Microsoft Excel**, **Power Query (ETL)**, and **Power Pivot (Data Modeling & DAX)**. 

The primary objective is to analyze historical performance across product categories, market segments, and regional logistics, providing actionable insights for revenue growth, profit margin optimization, and shipping speed efficiency.

---

## 🖼️ Dashboard Preview

![Superstore Dashboard] (docs/supersto: dashboard_preview.png)

---

## 🛠️ Data Architecture & Pipelines 


┌─────────────────┐       ┌─────────────────┐       ┌────────────────────────┐       ┌──────────────────────┐
│ Raw Data        │ ────> │ Power Query     │ ────> │ Power Pivot            │ ────> │ Interactive UI       │
│ (.xlsx / CSV)   │       │ Transformation  │       │ (Data Model & DAX)     │       │ (KPIs & Slicers)     │
└─────────────────┘       └─────────────────┘       └────────────────────────┘       └──────────────────────┘


1. **Extraction & Transformation (Power Query):**
   * Loaded raw sales, regional, and return tables.
   * Standardized data types (Currency, Order Dates, Category fields).
   * Handled duplicate records and missing values.

2. **Data Modeling (Power Pivot):**
   * Implemented a **Star Schema** relational data model.
   * Generated a dedicated **Calendar/Date Table** connected via 1-to-Many relationships to the main `Orders` fact table.

3. **DAX Measures Implementation:**
   Calculated key metrics directly in the data model for high performance:
   * **Total Sales:** `SUM(Orders[Sales])`
   * **Total Profit:** `SUM(Orders[Profit])`
   * **Profit Margin %:** `DIVIDE([Total Profit], [Total Sales], 0)`
   * **Prior Year Sales (PY Sales):** `CALCULATE([Total Sales], SAMEPERIODLASTYEAR('Calendar'[Date]))`
   * **YoY Sales Growth %:** `DIVIDE([Total Sales] - [PY Sales], [PY Sales], 0)`
   * **Avg Shipping Days:** `AVERAGE(Orders[Shipping Days])`

---

## 💡 Key Business Insights

* **Revenue Trends:** Consistent Year-over-Year (YoY) revenue growth across core market segments.
* **Profit Dynamics:** High-volume product categories exhibit varying profit margins, highlighting key opportunities for cost structure optimization.
* **Supply Chain Efficiency:** Average logistics fulfillment cycle maintained within target operational windows.

---


## 🛡️ License

This project is licensed under the MIT License. You are free to use, modify, and share this project with proper attribution.

## 🌟 About Me

Hi there! I'm Ahmed Alnaggar. I'm a data analyst.






