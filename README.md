# Sales Dashboard

## Problem Statement 

The goal of this analysis is to evaluate the sales performance of ABC Company in 2016 and 2017. This includes understanding
key metrics such as total sales, profit, and sales distribution across different categories, regions, and customer segments. 
The analysis aims to provide actionable insights to optimize sales strategies and improve business performance.

### Steps Followed
 - Download the Data.
 - Open the Data.
 - Clean the Data Find&Replace, Trim(), Remove Duplicates, Spelling, Number Format, Proper(), Data format check.
 - Create Pivot Table: add Order Date to rows and Sales, Profit to Values. Filter the date, select 2016 and 2017.
 - Calculate sales vs PY (Prior Year) and Profit vs PY. Use percentage formatting.
 - Add KPIs to the dashboard. Use shapes as background.
 - Create Pivot Table: add Sub-category to Rows and Order Date to Columns, add sales as values.
 - Filter the date (choose year 2016 and 2017), use Values Filter to display top 10 sub-categories.
 - Sort data by Sum of Sales Largest to Smallest.
 - Create Pivot Table: add City to Rows and Order Date to Columns, add sales as values.
 - Filter the date (choose year 2016 and 2017), use Values Filter to display top 10 states.
 - Sort data by Sum of Sales Largest to Smallest.
 - Add tables to Dashboard.
 - Calculate additional "vs PY" column. Use conditional cells formatting, insert symbols.
   
   
![formatting](https://github.com/user-attachments/assets/ec34ed8e-1581-44f9-83f7-237a8b8025be)
   
 - Use IF() formula to handle errors and blank cells.
 - Create Pivot Table: add Years, Quarters (Order Date) to Rows and Sales, Quantity as values.
 - Use relative reference to copy the table (Years, Quarters, Sum of Sales).
 - Calculate the Price in new column. Use currency formatting.
 - Set column chart, add 2nd data series to chart (Price). Change series type to line.
 - Create Pivot Table: add State to Rows and Sales as values.
 - Sort State Largest to Smallest. Create stacked colum chart.
 - Add two option buttons from Developer Tab, add text field (top 10/bottom 10).
 - Use SWITCH() and SORT() formula to copy te table and sort it as you wish.

		=SWITCH(G74,1,SORT(A75:B123,2,-1,FALSE),2,SORT(A75:B123,2,1,FALSE))

 - Use SWITCH() to change the chart's title (highest/lowest).

		=SWITCH(G74,1,"highest",2,"lowest")

 - Use CONCATENATE() to merge text.

	    =CONCATENATE("States with the ",I74," sales of all time")

 - Add slicers and set Report Connections, choose "Multi-select" option. 
  

# Report

Database : contains detailed sales data with columns such as Order ID, Order Date, Ship Date, Customer ID, 
Customer Name, Segment, Country, City, State, Postal Code, Region, Product ID, Category, Sub-Category, Product Name, 
Sales, Quantity, Discount, and Profit.

Workspace : contains pivot tables, tables, calculations.

Dashboard : contains key metrics, tables, charts, slicers.

# Report Snapshot

![Dashboard](https://github.com/user-attachments/assets/4e70e179-3251-4557-b81a-4abf40bb4a4f)

# Insights

Following interferences can be drawn from the report:

### [1] Regional Sales Performance:

	The South region is the top-performing region in terms of total sales, followed closely by the West and East 
	regions. The Central region has the lowest sales.

### [2] Product Category Contribution:

	Technology products is the highest-contributing category.

### [3] Monthly Sales Trends:

	There is a noticeable peak in sales during 4th quarter every year, likely due to holiday season promotions 
	and increased consumer spending. A dip in sales is observed in 1st quarter every year.

### [4] Customer Segment:
	
	The Consumer segment is the largest contributor to sales, indicating that individual consumers are the primary 
	target market. The Home Office segment is the smallest but stillsignificant.

### [5] Top Performing Products:

	The best selling products are very diverse. Some high-profit products are not necessarily the highest-selling.
