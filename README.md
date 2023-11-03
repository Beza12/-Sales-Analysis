# -Sales-Analysis

## Table of content

- [Project Overview](#project-overview)
- [Data Source](#data-source)
- [Data Preparation](#data-preparation)
- [Data Cleaning](#data-cleaning)
- [Analysis](#analysis)
- [Data Visualization](#data-visualization)
- [Summary](#summary)
### Project Overview

Atliq was established in 2017 as an IT services company to help businesses integrate their processes with automated tools. It is a company that supplies computer hardware and peripherals to many clients across India and USA. The company's head office is in Delhi and has a lot of regional offices across India

###### Atliq Hardware Sales Analysis
The company is facing issues in terms of its sales. The sales of the company have declined over the years. The company's Sales director is having a hard time tracking the sales in the dynamically growing market. When he wants to get insight into the sales in a particular region he will contact the regional managers for reports. But they would give him a lot of Excel files which make it difficult to get a clear insight. So he is interested in getting a visualized report that he can see clearly and the sales data and the areas the company need to focus on to increase sale.

The company has a sales management system that keeps track of all the sales so whenever they sell any computer or hardware this software prints the invoice of the sale. So it has all the records and store it in a MySQL database.

### Data Source
Sales data: The primary dataset used for this analysis is the 'db_dump_version_2' SQL file, containing detailed information about the sales the company made over the years.

#### Tools
- MySQL Workbench - SQL file source
- Power Query - data cleaning (transformation)
- PowerBI - Creating reports

### Data Preparation 
In the initial data preparation phase;
- Create a new connection on MySQL Workbench for the data we want to be stored.
- Import the SQL file into the created connection.
- After importing the file used different SQL queries to take a look at the data I will be working on.
- Create a connection with PowerBI.

### Data Cleaning
Use Power query to clean the data to use in the PowerBI desktop
- In the sales market we clear the row's null zone value
- In the transaction table we clear the -1 and o sales amount values
- Transforming the currency of the sales into Rupees
- Applying the changes and closing the Power query editor.

### Analysis 
Before creating the reports we need to create a data model where it shows a relationship between the tables. The desktop creates a model by default but we also add connections manually by dragging and dropping. We create a star schema by making the transaction table the focus table. 
We analyze the data by creating measures. On the desktop, we create a new table to record all the measures and it is a measure table. The measures are;
- Revenue - Get the total revenue by adding the sales amount 
- Sales quantity - Total sales quantity by adding sales Qty
- Total Profit Margin - the sum of profit margin
- Profit Margin % - divide the total profit margin by revenue
- Profit margin contribution % and Revenue contribution %

### Data Visualization
Start building the report using the measures created by dragging the measure into the build area. There are a lot of visualization options on the dashboard like line charts, pie charts, area charts, carts, tables, slicers, and many more. So we select from them to show the measures in a clear and understandable way.

In the measures, we can add different values to it to see it in different ways. Revenue by zone and by the market has a different outcome. So using the measures with different values helps to get more insight into the data.

### Summary 
 The report shows the real findings of the sales data. It shows the company sales by revenue, by profit by sales quantity, and many more across different years.
 Now the sales director can see what is going on with the sales and use it to make business decisions to increase sales.


