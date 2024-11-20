-----------------------------------------------------Superstore Sales Analysis------------------------------------------------

This project analyzes the Superstore Sales dataset from Kaggle using various data wrangling, analysis, and visualization techniques. 
The dataset provides information about sales transactions for a retail store,  including details like products, sales amount, customer information, and shipping details.

--Table of Contents
   1. Project Overview
   2. Technologies Used
   3. Setup and Installation
   4. Dataset
   5. Analysis and Insights
   6. Visualizations
   7. Contributing
   8. License

-------Project Overview

The goal of this project is to analyze the Superstore Sales dataset and uncover insights such as:

 Sales trends over time
 Top-performing regions and product categories
 Sales distribution by customer segment
 Profit margins and their relationship with sales
 Sales performance by shipping mode
 The analysis involves data cleaning, transformation, and visualization using Python and tools like Databricks


 ------Technologies Used

Databricks Community Edition: For data processing, transformation, and analysis.
Apache Spark: For distributed data processing.
Python: For data manipulation and analysis (via PySpark).
SQL: For querying the data within Databricks.
GitHub: For version control and project management.


------------Setup and Installation
To run this project locally, follow the steps below:

------------Clone this repository:


git clone https://github.com/yourusername/superstore-sales-project.git

-------------Install necessary Python libraries: You can install the required Python libraries using the following:

pip install pandas numpy matplotlib seaborn pyspark

------Set up Databricks:

Create a Databricks account (free).
Upload the Superstore Sales dataset (or use the dataset provided) to Databricks.
Execute the notebooks for data transformation and analysis.

---------Dataset


The dataset used in this project is from Kaggle’s Superstore Sales. It contains the following columns:

Row_ID: Row Identifier
Order_ID: Unique identifier for each order
Order_Date: Date the order was placed
Ship_Date: Date the order was shipped
Ship_Mode: Mode of shipment
Customer_ID: Unique identifier for each customer
Customer_Name: Name of the customer
Segment: Customer segment (e.g., Consumer, Corporate, Home Office)
Country: Country of the customer
City: City of the customer
State: State of the customer
Postal_Code: Postal code of the customer
Region: Region of the customer
Product_ID: Unique identifier for each product
Category: Product category (e.g., Furniture, Office Supplies, Technology)
Sub-Category: Sub-category of the product
Product_Name: Name of the product
Sales: Sales amount
Order_Month: Month of the order
Order_Year: Year of the order



------Analysis and Insights

The following insights were uncovered during the analysis:

------Sales by Region:

Sales were highest in the West region, followed by East and Central.

------Sales Trends Over Time:

Sales increased during the holiday seasons (e.g., November to December), showing a seasonal pattern.

-------Sales by Category:

The Technology category consistently outperformed other categories in sales.

--------Profit and Sales Correlation:

A strong correlation was observed between sales and profit, with certain categories like Technology having higher profit margins.

---------Sales Distribution by Customer Segment:

The Consumer segment contributed the highest to overall sales.

--------Visualizations

Several visualizations were created to better understand the data:

Sales by Region: Bar chart visualizing total sales per region.
Sales vs Profit: Scatter plot comparing sales and profit to identify profitable products.
Sales Trend Over Time: Line chart showing sales trends over the months and years.
Top Products by Sales: Bar chart displaying the top 10 products by total sales.
Sales by Ship Mode: Pie chart visualizing sales distribution across different shipping modes.


::::::License

MIT License

Copyright (c) [2024] [Bharathi_Dibbidi]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

![MIT License](https://img.shields.io/badge/License-MIT-blue.svg)




