# Amazon-Product-Review-and-Analysis

##About This Project
Excel Pivot Dashboard analyzing product sales, reviews, discounts, and pricing with KPI cards and slicers.

##Data Cleaning Actions

Before analysis, several data cleaning steps were applied to make the dataset analysis-ready.

###Steps:

. Product Name Shortening
To reduce long product names for cleaner charts:

=TRIM(LEFT(B2,FIND(" ",B2,FIND(" ",B2,FIND(" ",B2)+1)+1)))

. Proper Case Formatting
To standardize text casing:

=PROPER(C2)

. Removing Extra Spaces
For clean text fields:

=TRIM(C2)

. Category Simplification (Delimiters)
Split long category names (e.g., "Electronics - Mobile Accessories") using Text-to-Columns with delimiter:

Delimiter: "|"

Helper Columns
All columns used for calculations and cleaning were used in the creating the final dashboard.

