# Product Review and Discount Analysis Dashboard

This project is a detailed Excel dashboard analysis of an e-commerce product dataset. It explores product ratings, discounts, pricing patterns, and customer reviews across various product categories.

## Data Source

**Digital Skill Africa (The Incubator Hub)**  
Dataset provided during a data analysis training program.  
File analyzed: `Amazon Case Study(Excel Format)`

---

## Data Cleaning Actions

1. **Standardized Product Names**  
   Applied `=TRIM(LEFT(B2,FIND(" ",B2,FIND(" ",B2,FIND(" ",B2)+1)+1)))` to shorten long product names for pivot charts.

2. **Proper Case Formatting**  
   Used `=PROPER(C2)` to format all text fields consistently (e.g., product names, categories).

3. **Column Hiding**  
   Only Original product name and the column with the Trim function are hidden.

4. **Category Simplification with Delimiters**  
   Used Excel delimiter tools to split and clean category names for easier grouping and pivoting.

5. **Converted Currency Text to Numbers**  
   Replaced 13,9,900 to 139,900 using Replace values.

6. **Created Price Range Buckets**  
   Added a helper column:
 =IF(Price<200,"<₹200",IF(Price<=500,"₹200–₹500",">₹500"))

7. **Discount Calculations**  
Calculated discount percentage and applied logic:
  =IF(Discount>=0.5, 1, 0)

## Analysis Tasks

These business questions were answered using PivotTables, charts, helper columns, and calculated fields:

1. What is the average discount percentage by product category?  
2. How many products are listed under each category?  
3. What is the total number of reviews per category?  
4. Which products have the highest average ratings?  
5. What is the average actual price vs. the discounted price by category?  
6. Which products have the highest number of reviews?  
7. How many products have a discount of 50% or more?  
8. What is the distribution of product ratings (e.g., 3.0, 4.0, etc.)?  
9. What is the total potential revenue (Actual Price × Rating Count) by category?  
10. How many unique products fall into each price range bucket?  
11. How does rating relate to the level of discount?  
12. How many products have fewer than 1,000 reviews?  
13. Which categories have products with the highest discounts?  
14. Identify the top 5 products in terms of rating and number of reviews combined.



## KPI Summary (from Excel Dashboard)

| Metric                          | Value        | Insight |
|--------------------------------|--------------|---------|
| Total Products                 | 1350         | Unique products analyzed |
| Number of Categories           | 1350         | Suggests category duplication; cleaned during processing |
| Total Potential Revenue        | ₹ 14B+       | Based on price × review count |
| Average Rating Overall         | 4.09         | Indicates high customer satisfaction |
| Total Reviews                  | 2,380,431    | High engagement from users |
| Average Discount               | 47%          | Aggressive discounting across most products |
| Products with ≥50% Discount    | 602          | Nearly half of all products are heavily discounted |




## Key Insights from the Dashboard

- **High Discount Prevalence:** Nearly half of all products (over 600) have discounts of 50% or more, suggesting aggressive price-cutting as a competitive strategy.
- **Customer Engagement:** The dataset shows over 2.3 million reviews across all products, with an average rating above 4.0, indicating strong user activity and overall product satisfaction.
- **Top Performing Products:** Products that rank highest in both rating and number of reviews tend to be in electronics and smartphone categories.
- **Category Revenue Trends:** Categories like Mobiles and Laptops generate significantly more potential revenue based on actual price × review count.
- **Price Distribution:** Most products fall in the ₹200–₹500 and >₹500 ranges, indicating a focus on mid-to-premium pricing segments.
- **Slicer Interactivity:** The dashboard allows real-time filtering by category, helping users focus on specific segments and observe how KPIs and charts respond dynamically.

These insights enable stakeholders to make better marketing, pricing, and inventory decisions based on customer feedback, price sensitivity, and product popularity.




## Dashboard Screenshots

### Full Dashboard Overview
![Dashboard_Overview](https://github.com/user-attachments/assets/9745b8c1-d65b-46b8-9fe8-7184148a03c7)

### KPI cards
![KPI_Cards](https://github.com/user-attachments/assets/b73cef6b-3028-4c92-8f2f-3cd067abdca2)

### Top 5 Products (By Rating*Reviews)
![Top-5-Product](https://github.com/user-attachments/assets/c7562ad6-bffc-4761-947a-0d6bddb1c637)

### Discount Distribution by Category
![Category-Discount-Distribution](https://github.com/user-attachments/assets/97e41fe4-a8ed-4440-9682-b317b1bc5644)

### Rating Distribution
![Rating-Distribution](https://github.com/user-attachments/assets/5eac7d82-9e8c-470f-a642-5cc73554dc1b)

### Price Range Distribution
![Price-Range-Distribution](https://github.com/user-attachments/assets/43f2b6dd-833f-482e-aeb8-839bb895db21)

### Slicer Filter Example
![slicer](https://github.com/user-attachments/assets/574841c1-43c6-4c92-9de2-108ea61deb65)





## Tools Used

- Microsoft Excel 2016
- Pivot Tables
- Pivot Charts
- Dynamic KPIs
- Slicers
- Helper Columns & Logical Formulas



## How to Use This Project

1. Open `Product Dashboard.xlsx` from the root folder.
2. Use the slicer to filter by category or other fields.
3. Observe how KPIs and charts update dynamically.
4. Review the screenshots for reference if Excel is unavailable.


## Contact

**Henry Ezeh Chukwuebuka**  
Data Analyst | Nigeria  
Email: `ezehebuka94@yahoo.com`  
GitHub: [@DataEzeh](https://github.com/DataEzeh)
