# Superstore-Supply-Chain-Analysis
## **Table of Contents** <br>
- [Project Overview](#project-overview) <br>
- [Technology and Skills](#technology-and-skills)
- [Project Objectives](#project-objectives)
- [Workbook Structure](#workbook-structure)
- [Key Insights](#key-insights)
- [Reommendations](#recommendations)

## Project Overview

This document provides an analysis of a Superstore's end-to-end supply chain and logistics operations. Metrics reviewed include sales across multiple locations, product category, customer segment and time unit. This dataset, sourced from Kaggle, a widely recognized platform offering copyright-free datasets, contains a single sheet with 23
columns and 100 rows. The data set includes 3 product lines Skincare, Haircare, and Cosmetics. The analysis was conducted using and Microsoft Excel for data cleaning, analysis, and visualization.

## Technology and Skills
- **Technology**: Excel
- **Skills**: Data cleaning, data analysis, data visualization/dashboarding

## Project Objectives
The primary goals of this project were:

+ To analyze the supply chain data.
+ Identify key performance metrics for operational efficiency.
+ Develop an interactive dashboard to visualize trends.
+ Facilitate data-driven decisions that improve the supply chain process and enhance customer satisfaction.

## Workbook Structure
The workbook Supply_Chain_Project.xlsx contains 7 sheets, split into the raw dataset, cleaned data and derived analysis sheets.

### 1. `Raw_data`
+ Columns: `Product type`, `SKU`, `Price`, `Availability`, `Number of products sold`, `Revenue generated`, `Customer demographics`, `Stock levels`, `Supplier lead times`, `Shipping carriers`, `Shipping times`, `Order quantities`, `transportation modes`, `routes`, `manufacturing lead time` for every SKU.

+ The raw dataset of the company, includes the three product types being shipped (skincare, haircare, and cosmetics), the four routes to supplying the products (air, sea, road, and rail) and the five suppliers. It contains revenue generated, costs, lead times and inventory levels.

### 2. `Clean_data`
+ Column: `Total Cost`, `Revenue per unit`

+ I checked for any missing values. I identified Manufacturing costs and calculated Total costs, estimated profits and profit margins for each transaction.

### 3. `KPIs`
+ A single-page executive scorecard built entirely from live formulas, including:

+ **Sales KPIs**
  - Total Revenue - `SUM` of all revenue generated
  - Total Units Sold - `SUM` of Number of products sold
  - Average Price - `AVERAGE` of Price
  - Average Revenue per Unit - `AVERAGE` of Revenue per unit`

+ **Inventory KPIs**
  - Average Stock Level - `AVERAGE` of Stock level
  - Total Stock - `SUM` of stock level
  - Average Availability - `AVERAGE` of Availabilty
  - Average Inventory Efficiency- `AVERAGE` of Inventory Efficience

+ **Profitability KPIs**
  - Total Manufacturing Cost - `SUM` of Manufacturing Cost
  - Total Shipping Cost - `SUM` of the shipping cost
  - Total Transportation Cost - `SUM` of Transportation cost
  - Estimated Total Cost - `SUM` of the total cost (transportation cost, shipping cost, and other costs)
  - Estimated Total Profit - Total Revenue - Total Cost
  - Average Profit - `AVERAGE` of Estimated Profit
  - Average Profit Margin - `SUM` of Estimated Profit / `SUM` of Revenue generated

+ **Supplier KPIs**
  - Number of Suppliers - `COUNTA(UNIQUE())` of Supplier Name
  - Average Supplier Lead Time - `AVERAGE` of Supplier Lead time
  - Average Manufacturing Cost - `AVERAGE` of manufacturing cost

+ **Quality KPIs**
  - Average Defect Rate - `AVERAGE` of defect rates
  - Failed Inspections - `COUNTIF(Clean_Data[Inspection results],"Fail")`
  - Inspection Pass Rate - `COUNTIF(Clean_Data[Inspection results],"Pass")/COUNTA(Clean_Data[Inspection results])`

+ **Logistics KPIs**
  - Average Shipping Time - `AVERAGE` of Shipping time
  - Total Shipping Cost - `SUM` of shipping cost
  - Average Shipping Cost - `AVERAGE` of shipping cost
  - Average Shipping Cost per Unit - `AVERAGE` of shipping cost per unit
  - Average Total Lead Time - `AVERAGE` of Total Lead Time

### 4. `Pivot_Analysis`
+ A total of 5 pivot tables is available on this sheet, **REVENUE BY PRODUCT TYPE, SUPPLIER PERFORMANCE, TRANSPORTATION ANALYSIS, ROUTE ANALYSIS, QUALITY ANALYSIS**

 - REVENUE BY PRODUCT TYPE - a pivot table containing Product Type, Total Revenue Total Units Sold.
 - SUPPLIER PERFORMANCE - contains Supplier Name, Avg Supplier Lead Time, Avg Defect rates, Avg Manufacturing costs, and Total Production volumes
 - TRANSPORTATION ANALYSIS - contains transportation modes, Avg Shipping Times, Avg Shipping Costs and Total Shipping Costs
 - ROUTE ANALYSIS - contains Transportation routes, Avg Supplier costs, Avg Shipping Times, and Total Revenue
 - QUALITY ANALYSIS - contains the three products types and their corresponding Avg Defect Rates.

### 5. `Charts`
- There are six charts on this sheet, **Revenue By Product Type, Revenue vs Estimated Profit, Shipping cost by Transportation Mode, Supplier Defect Rate, Shipping Time by Transportation Mode, Lead Time vs Defect Rate**

### 6. `Deeper Analysis`
The correlation between Price and Number of Products Sold, Shipping time and Shipping costs, and Manufacturing Lead time and Defect rates was calculated and examined on this sheet. Two other pivot tables was also done to give a better understanding on the data insights.

### 7. `Dashboard`
- The final Dashboard to visualize trends in the supply chain.
<img width="695" height="566" alt="Screenshot (31)" src="https://github.com/user-attachments/assets/b36c9cb4-f157-41a6-957e-004879d7e56d" />

## Key Insights
+ Total Revenue Generated is $577,604.82 and Total Profit is $456,048.57, and Total Units Sold is 46,726 units of which is skincare is the highest contributor on all counts and Cosmetics has the least amount of units sold and makes the least revenue and profit. 
+ There is an Average Profit Margin of 78.96%. More revenue is retained as profit relative to sales.
+ Supplier 5 has the most defect rates of 2.67% and Supplier 1 has the least amount of defect rates, 1.8%
+ There is no strong visible relationship between Lead Time and Defect Rates. Longer lead times do not consistently mean more defects  and high defect rates of 4% to 5% occur across different lead times.
+ There is a negative correlation between shipping times and shipping costs, little or no linear relationship between price and units sold and little to no correlation between manufacturing lead time and defect rates. Tis means that there is no visible relationship between, shipping times and shipping costs, manufacturing lead time and defects rates, and price and number of units sold.
+ Sea has the highest average shipping time, 7.12 days, but the least amount of shipping cost, $11,275.00.
+ Skincare has more sales compared with its recorded stock than Haircare and Cosmetics. Skincare has an Inventory Efficiency ratio of 12.71, Haircare has an Inventory Efficiency ratio 8.54 and, Cosmetics has an Inventory Efficiency ratio of 7.71

## Recommendations
+ A differentiated transportation strategy should be  used rather than relying on one mode for every shipment. The mode should be chosen based on urgency, route, shipment size, and cost per unit. Sea should be used for planned, less time-sensitive shipments and prioritize faster modes for urgent orders. Road, for example, has the lowest average shipping time of 4.72 days but has the second most expensive shipping cost so should be used for urgent orders.
+ Skincare stock should be monitored carefully so that strong demand does not lead to stockouts. Skincare should be considered to find out if more stock is needed to support demand, based on sales forecast.
+ An observation of defect rates of 4% or higher is seen across various the suppliers and product types and regardless of lead time. A further investigation on production conditions should be done to find causation of the defects.





	
