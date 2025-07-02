# Product Sales & Review Dashboard (Excel Pivot Analysis)

---

## Project Description

This project presents an Excel-based **Sales & Review Analysis Dashboard**, built using **Pivot Tables**, **Charts**, **KPI Cards**, and **Slicers** to explore customer buying patterns, pricing strategy, discount effects, and product popularity.  

It answers business questions like:

- Which categories offer the highest discounts?  
- Which products are best-rated and most-reviewed?  
- What is the potential revenue per product?  
- How do ratings relate to discount levels?

The project was done as part of a **Data Analysis training** with **Digital Skill Africa (The Incubator Hub)**.

---

## Data Cleaning Steps

Before building the dashboard, the raw dataset was cleaned for quality and usability:

| Task | Excel Formula or Action |
|------|--------------------------|
| Shortened Product Names | `=TRIM(LEFT(B2,FIND(" ",B2,FIND(" ",B2,FIND(" ",B2)+1)+1)))` |
| Proper Case Formatting | `=PROPER(C2)` |
| Removed Extra Spaces | `=TRIM(C2)` |
| Simplified Category Names | Used `Text to Columns` (delimiter: "-") |
| Created Helper Columns | For discounts, price ranges, ratings buckets |
| Hidden Formula Columns | To clean the final sheet before dashboarding |

---

## Business Questions Answered

Below are the key questions the analysis answers:

| Question | Method |
|---------|--------|
| **1. Avg. Discount % by Category** | Pivot Table: Average of Discount % |
| **2. Total Products per Category** | Pivot Table: Count of Product Name |
| **3. Total Reviews per Category** | Pivot Table: Sum of Rating Count |
| **4. Highest Average-Rated Products** | Pivot Table: Avg. Rating by Product |
| **5. Avg. Actual vs Discounted Price** | Pivot Table: Category comparison |
| **6. Products with Most Reviews** | Pivot Table: Sort by Review Count |
| **7. Products with ≥50% Discount** | Helper Column + Pivot Count |
| **8. Rating Distribution (3.0, 4.0, etc.)** | Pivot: Count by Rounded Rating |
| **9. Potential Revenue per Category** | Helper Column: `=Actual Price × Rating Count` |
| **10. Products per Price Range** | Helper:  
`=IF(D2<200,"<₹200",IF(D2<=500,"₹200–₹500",">₹500"))` |
| **11. Rating vs Discount Relation** | Discount buckets + Avg Rating |
| **12. Products with <1,000 Reviews** | Helper Column: `=IF(Count<1000,1,0)` |
| **13. Categories with Max Discounts** | Pivot Table: Max of Discount % |
| **14. Top 5 Products (Rating × Reviews)** | Helper:  
`=Rating * Review Count` |

---

## Dashboard Components

| Section | Details |
|--------|---------|
| **Top KPIs** | Total Products, Avg Rating, Total Reviews, ≥50% Discount Products, Total Revenue |
| **Slicers** | Used for **Category** and **Price Range** |
| **Pivot Charts** | Clustered Columns, Bar Charts, KPI Cards |
| **Filters** | Slicer-driven (no dropdowns used) |
| **Formatting** | Only **Revenue KPI** formatted in **Billions** using:  
`#,##0,,,"B"` |

---

## Excel Features Used

- Pivot Tables  
- Pivot Charts  
- KPI Cards using `GETPIVOTDATA`  
- Slicers (not dropdowns)  
- Helper columns for logic (e.g., discount ≥50%, buckets, weighted scores)  
- Custom formatting (`#,##`)  
- No Power BI, no VBA, no macros

---

## Folder Structure

```plaintext
📦 Product-Sales-Dashboard
├── 📄 README.md
├── 📊 Excel Dashboard (.xlsx)
├── 📁 Screenshots/
│   ├── dashboard-overview.png
│   ├── kpi-cards.png
│   ├── slicers.png
│   └── pivot-charts.png
