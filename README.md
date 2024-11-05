# LITA_CAPSTONE_PROJECT-SALES_DATA-

### PROJECT OVERVIEW:
Making reference to the data and capstone project document shared earlier, by analyzing the sales performance of a retail store and carrying out the following exploratory process of the sales data to uncover key insights such as
- Top Selling Products
- Regional Performances
- Monthly Sales Trend and
By telling a compelling story and building an interactive dashboard Power Bi report: **To gather insight, Highlight findings And making business decisions.**

### DATA DESCRIPTION:
This dataset includes the following Columns:
- Order Number
- Customer Id
- products
- region
- Order Date
- Quantity
- Unit Price
  
### DASH BOARD REVIEW
- Customer Id
- products: Items sold in the store
- region: The other regional branches of the store ( North, South, East West) 
- Order Date: Date order was palced
- Quantity: The number of units of the product ordered in each transaction
- Unit Price: The aquisition cost per unit of the product

### STATISTICS ABOUT THE DATASET:
Number of Unique Customers: 50,000
Number of Products: 6
Total Sales: 10587500 ![image](https://github.com/user-attachments/assets/e260abe1-8773-4574-ac85-2f3f97b30e34)
Total Region: 4 

### METHODOLOGY

#### Data Collection
The dataset for this analysis was provided by LITA_ The Incubator Hub for leaening and training purposes. The data was provided in Excel sheet [download Here] (https://canvas.instructure.com/files/273182802/download?download_frd=1) or https://eu.docworkspace.com/d/sILre1-uDAsKJzrgG?sa=wa&ps=1&fn=LITA%20Capstone%20Dataset%20(1).xlsx
 The excel sheet making it accessible to 
- analyse the excel sheet
  The excel sheet was further converted to CSV format for easy importing of files into:
  - SQL to write various queries
  - Power BI to create dashboards using various charts (pieChart and clustered Column Chart)

### DATA ANALYSIS

#### Calculation in Excel
- *Generating Total Sales* ```(=F2* G2)```
- *calculating average sales by product* 
``` =AVERAGEIF($C1:$C50001,$C2,$H1:$H50001)```
#### Queries in SQL
- SQL
  1. ```Select product,
     sum(quantity*unitprice) as totalsale
 ```From [dbo]
 ```Group by product;
 
  2. ```Select region,
     count(*) as NumberOfTransactions
```From [dbo]
```Group by region;

3. ```select top 1 product, sum(quantity*unitprice) as totalsales
```From [dbo]
```Group by product
```Order by totalsales desc;```

4. ```Select month(OrderDate) as month, sum(quantity*unitprice) as MonthlySales
```From [dbo]
```Where year(OrderDate) = year(GetDate())
```Group by month(OrderDate)
```Order by month;

 


### DASH BOARD OVERVIEW
