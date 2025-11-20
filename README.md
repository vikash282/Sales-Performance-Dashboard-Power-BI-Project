# Sales-Performance-Dashboard-Power-BI-Project
⭐ Project Overview
This project is a fully interactive Sales Performance Dashboard built using Power BI, DAX, and Excel.
The goal of the dashboard is to provide deep insights into sales trends, customer performance, regional performance, category-wise breakdown, and profitability metrics.
The dashboard helps businesses:
Track revenue & profit over time
Identify top customers
Compare category performance
Analyze high/low performing regions
Monitor KPIs like Profit Margin, Discount %, Quantity sold
Make data-driven decisions quickly
Sales_Dashboard_Project/
│
├── Dataset/
│   └── Orders.xlsx  (Cleaned Dataset)
    |__ Orders full.xlsx (Original Dataset)
│
├── PowerBI_File/
│   └── Order_report.pbix
│
├── Documentation/
│   ├── Project_Report.pdf
│
├── Exports/
│   ├── Dashboard_Screenshot.png
│   └── Dashboard_PDF.pdf
│
⭐ Dashboard Features
A complete end-to-end BI project for sales analysis, insights, KPIs &amp; reporting.
Dashboard Features
1️⃣ Key Performance Indicators (KPIs)
The dashboard displays the following metrics using DAX:
Total Sales
Total Profit
Profit Margin (%)
Total Quantity Sold
Average Discount (%)
These KPIs provide a quick overview of business performance.

2️⃣ Sales Trend Over Time (Line Chart)
Shows how total sales changed month to month.
Uses a Date Table for proper time intelligence.
Includes smooth line for visual clarity.

3️⃣ Sales by Category (Bar Chart)
Breakdown of sales by:
Furniture
Technology
Office Supplies
Useful to identify best-selling product categories.

4️⃣ Sales by Region (Filled Map)
Visualizes global sales performance across:
Central
East
West
South
Europe
Oceania
Africa
Shows top-performing and weak regions.

5️⃣ Top 10 Customers by Sales
Horizontal bar chart showing:
Highest revenue-generating customers
Helping with customer segmentation, loyalty programs, upselling strategies

6️⃣ Interactive Slicers
Filters included:
Segment
Category
Region
Allows users to dynamically explore insights.

⭐ DAX Measures Used
Total Sales
Total Sales = SUM('Sheet1'[Sales])

Total Profit
Total Profit = SUM('Sheet1'[Profit])

Profit Margin
Profit Margin = DIVIDE([Total Profit], [Total Sales], 0)

Total Quantity
Total Quantity = SUM('Sheet1'[Quantity])

Average Discount
Average Discount = AVERAGE('Sheet1'[Discount])

Time Intelligence Measures
Date Table
DateTable = CALENDAR(MIN('Sheet1'[Order Date]), MAX('Sheet1'[Order Date]))

Last Year Sales
Total Sales LY = CALCULATE([Total Sales], SAMEPERIODLASTYEAR(DateTable[Date]))

YoY Growth
YoY Growth = DIVIDE([Total Sales] - [Total Sales LY], [Total Sales LY], 0)


⭐ Tools Used
Power BI Desktop
Microsoft Excel
Power Query
DAX (Data Analysis Expression)

⭐ Dataset Details
dataset contains columns:
Column                    Description
Order ID                  Unique order identifier
Order Date                Date of purchase
Customer Name             Buyer 
Segment                   Consumer / Corporate / Home Office
City, State, Country      Geo details
Region                    Region mapping
Category                  Product category
Product Name              Product description
Sales                     Revenue
Profit                    Profit amount
Quantity                  Units sold
Discount                  Discount applied

⭐ How to Run the Dashboard
Download the .pbix file
Open Power BI Desktop
Load sales_data.xlsx if needed
View dashboard, insights & slicers

⭐Conclusion
This Sales Performance Dashboard provides actionable insights and helps management quickly interpret sales data.
