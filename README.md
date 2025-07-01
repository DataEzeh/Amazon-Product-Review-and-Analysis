# Amazon-Product-Review-and-Analysis

## About This Project
Excel Pivot Dashboard analyzing product sales, reviews, discounts, and pricing with KPI cards and slicers.

## Data Cleaning Actions

Before analysis, several data cleaning steps were applied to make the dataset analysis-ready.

### Steps:

- Product Name Shortening
To reduce long product names for cleaner charts:

=TRIM(LEFT(B2,FIND(" ",B2,FIND(" ",B2,FIND(" ",B2)+1)+1)))

- Proper Case Formatting
To standardize text casing:

=PROPER(C2)

- Removing Extra Spaces
For clean text fields:

=TRIM(C2)

- Category Simplification (Delimiters)
Split long category names (e.g., "Electronics - Mobile Accessories") using Text-to-Columns with delimiter:

Delimiter: "|"

- Helper Columns
All columns used for calculations and cleaning were used in the creating the final dashboard.


## Business Questions Answered (Task List)

Below are the business questions answered using Pivot Tables, Calculated Columns, and Formulas.

1. Average Discount Percentage by Product Category

Pivot Table

Rows: Category

Values: Average of Discount %



---

2. Total Number of Products per Category

Pivot Table

Rows: Category

Values: Count of Product Name



---

3. Total Number of Reviews per Category

Pivot Table

Rows: Category

Values: Sum of Rating Count



---

4. Products with the Highest Average Ratings

Pivot Table

Rows: Product Name

Values: Average of Rating

Sort: Descending by Average Rating



---

5. Average Actual Price vs Discounted Price by Category

Pivot Table

Rows: Category

Values: Average of Actual Price, Average of Discounted Price



---

6. Products with the Highest Number of Reviews

Pivot Table

Rows: Product Name

Values: Sum of Rating Count

Sort: Descending



---

7. Products with Discount ≥ 50%

Helper Column Formula:

=IF([@[Discount %]]>=0.5,1,0)

Pivot Table:

Values: Sum of helper column




---

8. Distribution of Product Ratings

Pivot Table

Rows: Rating (or rounded rating)

Values: Count of Product Name



---

9. Total Potential Revenue by Category

Helper Column Formula:

=[@[Actual Price]]*[@[Rating Count]]

Pivot Table:

Rows: Category

Values: Sum of Total Revenue


KPI Card Formatting for this Metric Only:

#,##0,,,"B"


(Displayed in Billions only on the KPI card)


---

10. Unique Products per Price Range Bucket

Helper Column Formula:

=IF(D2<200,"<₹200",IF(D2<=500,"₹200–₹500",">₹500"))

Pivot Table:

Rows: Price Range Bucket

Values: Count of Product Name




---

11. Relationship Between Rating and Discount Level

Discount Buckets: Created using formulas or manual grouping.

Pivot Table:

Rows: Discount Range Bucket

Values: Average Rating




---

12. Products with Fewer Than 1,000 Reviews

Helper Column Formula:

=IF([@[Rating Count]]<1000,1,0)

Pivot Table:

Values: Sum of helper column




---

13. Categories with Highest Discounts

Pivot Table:

Rows: Category

Values: Max of Discount %




---

14. Top 5 Products Based on Rating × Review Count

Helper Column Formula:

=([@[Rating]]*[@[Rating Count]])

Pivot Table:

Rows: Product Name

Values: Sum of Weighted Score

Filter: Top 5
