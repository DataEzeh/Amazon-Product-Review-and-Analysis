# Amazon-Product-Review-and-Analysis
Excel Pivot Dashboard analyzing product sales, reviews, discounts, and pricing with KPI cards and slicers.
Data Cleaning Steps (Before Analysis)

The raw dataset had multiple issues like:

Very long product names (difficult for charts)

Inconsistent capitalization in text fields

Extra unwanted spaces in text

Category names that were too detailed for analysis



 Cleaning Actions Performed:Issue	Solution

Long Product Names (for cleaner chart labels)	Formula Used:
=TRIM(LEFT(B2,FIND(" ",B2,FIND(" ",B2,FIND(" ",B2)+1)+1)))	
 Kept first 3 words from Product Name	
 
Inconsistent Capitalization (mixed upper/lower cases)	Formula Used:
=PROPER(C2)	
 Applied to Product Names. 

 Removing of Duplicates from Product_ID and Product_Name
 
Extra Spaces	Formula Used:
=TRIM(C2)	
 Cleaned unwanted spaces	
 
Too-Long Category Names (e.g., “Electronics - Mobile Accessories”)	Used Text-to-Columns → Delimiter: "|"
 Retained only the main category	
Helper Columns Management, all helper columns except Product_Name on column 2 and trimmed on column 3 were hidden. 
