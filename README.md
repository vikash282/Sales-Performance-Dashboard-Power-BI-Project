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

```text
Sales_Dashboard_Project/
│
├── Dataset/
│   ├── Orders.xlsx       (Cleaned Dataset)
│   └── Orders full.xlsx  (Original Dataset)
│
├── PowerBI_File/
│   └── Order_report.pbix
│
├── Documentation/
│   └── Project_Report.pdf
│
└── Exports/
    ├── Dashboard_Screenshot.png
    └── Dashboard_PDF.pdf
🚀 Dashboard FeaturesA complete end-to-end BI project for sales analysis, insights, KPIs & reporting.1️⃣ Key Performance Indicators (KPIs)The dashboard displays the following metrics using DAX to provide a quick overview of business performance:Total SalesTotal ProfitProfit Margin (%)Total Quantity SoldAverage Discount (%)2️⃣ Sales Trend Over Time (Line Chart)Shows how total sales changed month to month.Uses a Date Table for proper time intelligence.Includes a smooth line for visual clarity.3️⃣ Sales by Category (Bar Chart)Breakdown of sales to identify best-selling product categories:FurnitureTechnologyOffice Supplies4️⃣ Sales by Region (Filled Map)Visualizes global sales performance across different regions to show top-performing and weak areas:Central, East, West, SouthEurope, Oceania, Africa5️⃣ Top 10 Customers by SalesHorizontal bar chart showing the highest revenue-generating customers. This helps with:Customer segmentationLoyalty programsUpselling strategies6️⃣ Interactive SlicersAllows users to dynamically explore insights by filtering:SegmentCategoryRegion🧮 DAX Measures UsedBelow are the specific DAX formulas used to calculate the metrics in this dashboard.Key MeasuresCode snippetTotal Sales = SUM('Sheet1'[Sales])

Total Profit = SUM('Sheet1'[Profit])

Profit Margin = DIVIDE([Total Profit], [Total Sales], 0)

Total Quantity = SUM('Sheet1'[Quantity])

Average Discount = AVERAGE('Sheet1'[Discount])
Time Intelligence MeasuresCode snippet/* Date Table Creation */
DateTable = CALENDAR(MIN('Sheet1'[Order Date]), MAX('Sheet1'[Order Date]))

/* Sales Last Year */
Total Sales LY = CALCULATE([Total Sales], SAMEPERIODLASTYEAR(DateTable[Date]))

/* Year over Year Growth */
YoY Growth = DIVIDE([Total Sales] - [Total Sales LY], [Total Sales LY], 0)
🛠 Tools UsedPower BI Desktop (Dashboarding & Visualization)Microsoft Excel (Data Source)Power Query (Data Cleaning & Transformation)DAX (Data Analysis Expressions)📄 Dataset DetailsThe dataset contains the following columns:ColumnDescriptionOrder IDUnique order identifierOrder DateDate of purchaseCustomer NameName of the buyerSegmentConsumer / Corporate / Home OfficeCity, State, CountryGeographical detailsRegionRegion mappingCategoryProduct categoryProduct NameProduct descriptionSalesRevenue generatedProfitProfit amountQuantityUnits soldDiscountDiscount applied💻 How to Run the DashboardDownload the .pbix file from the PowerBI_File/ folder.Open Power BI Desktop.Load the Orders.xlsx dataset if the path needs refreshing.Interact with the dashboard using the slicers and visuals.⭐ ConclusionThis Sales Performance Dashboard provides actionable insights and helps management quickly interpret sales data to drive business growth.
