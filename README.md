# Sales Performance Dashboard - Power BI Project

## ⭐ Project Overview
This project is a fully interactive **Sales Performance Dashboard** built using **Power BI, DAX, and Excel**. 

The goal of the dashboard is to provide deep insights into sales trends, customer performance, regional performance, category-wise breakdown, and profitability metrics.

**The dashboard helps businesses:**
* Track revenue & profit over time.
* Identify top customers.
* Compare category performance.
* Analyze high/low performing regions.
* Monitor KPIs like Profit Margin, Discount %, and Quantity sold.
* Make data-driven decisions quickly.

---

## Project Structure

Sales_performance/
│
├── Dataset/
│   ├── Orders.xlsx       (Cleaned Dataset)
│   └── Orders full.xlsx  (Original Dataset)
│
├── PowerBI_File/
│   └── Order_report.pbix
│
├── Documentation/
│   └── Data cleaning and prepration.pdf
│
└── Exports/
    ├── Dashboard.pdf
    
    
### Dashboard FeaturesA complete end-to-end BI project for sales analysis, insights, KPIs & reporting.
1️⃣ Key Performance Indicators (KPIs)
The dashboard displays the following metrics using DAX to provide a quick overview of business performance:
Total SalesTotal Profit, Profit Margin (%), Total Quantity Sold, Average Discount (%)
2️⃣ Sales Trend Over Time (Line Chart) Shows how total sales changed month to month. Uses a Date Table for proper time intelligence.Includes a smooth line for visual clarity.
3️⃣ Sales by Category (Bar Chart)Breakdown of sales to identify best-selling product categories: Furniture Technology Office Supplies
4️⃣ Sales by Region (Filled Map) Visualizes global sales performance across different regions to show top-performing and weak areas:Central, East, West, SouthEurope, Oceania, Africa
5️⃣ Top 10 Customers by SalesHorizontal bar chart showing the highest revenue-generating customers. This helps with: Customer segmentationLoyalty programsUpselling strategies
6️⃣ Interactive SlicersAllows users to dynamically explore insights by filtering:Segment, CategoryRegion

### DAX Measures Used
Below are the specific DAX formulas used to calculate the metrics in this dashboard.
Total Sales = SUM('Sheet1'[Sales])

Total Profit = SUM('Sheet1'[Profit])

Profit Margin = DIVIDE([Total Profit], [Total Sales], 0)

Total Quantity = SUM('Sheet1'[Quantity])

Average Discount = AVERAGE('Sheet1'[Discount])

### Time Intelligence Measures
/* Date Table Creation */
DateTable = CALENDAR(MIN('Sheet1'[Order Date]), MAX('Sheet1'[Order Date]))

/* Sales Last Year */
Total Sales LY = CALCULATE([Total Sales], SAMEPERIODLASTYEAR(DateTable[Date]))

/* Year over Year Growth */
YoY Growth = DIVIDE([Total Sales] - [Total Sales LY], [Total Sales LY], 0)

🛠 Tools UsedPower BI Desktop (Dashboarding & Visualization)Microsoft Excel (Data Source)Power Query (Data Cleaning & Transformation)DAX (Data Analysis Expressions)
## Dataset DetailsThe dataset contains the following columns:
Column                 Description
Order ID               Unique order identifier
Order Date             Date of purchase
Customer Name          Name of the buyer
Segment                Consumer / Corporate / Home Office
City, State, Country   Geographical details
Region                 Region mapping
Category               Product category
Product Name           Product description
Sales                  Revenue generated
Profit                 Profit amount
Quantity               Units sold
Discount               Discount applied

*** How to Run the Dashboard
Download the .pbix file from the PowerBI_File/ folder.

Open Power BI Desktop.

Load the Orders.xlsx dataset if the path needs refreshing.

Interact with the dashboard using the slicers and visuals.

### Conclusion
This Sales Performance Dashboard provides actionable insights and helps management quickly interpret sales data to drive business growth.
