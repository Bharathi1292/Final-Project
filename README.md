# Final-Project

# Project Name::::Superstore Data Analysis

## Description
This project demonstrates how to clean, transform, and analyze **Superstore sales data** using **Apache Spark** and **Delta Lake** on **Databricks**. The analysis covers:

1. Data Cleaning: Removing or handling missing and irrelevant data.
2. Data Transformation (Feature Engineering) : Creating new columns to enhance analysis, such as profit margin and time-based 
features (month, year).
3. Data Aggregation : Summarizing key metrics like total sales, total profit, etc., by different dimensions (e.g., Category,Region).
4. Data Storage : Storing the processed data in a Delta table format for further analysis or sharing.

## Prerequisites

- Databricks Community Edition account (free tier available)
- Spark 3.x and Delta Lake  (pre-configured on Databricks)
- Superstore dataset (can be uploaded in formats like CSV, Parquet, or Delta)

## Setup and Installation

### 1. Importing Data into Databricks

Upload the Superstore dataset into Databricks using the **DBFS** (Databricks File System), either in **CSV**, **Parquet**, or **Delta** format. You can use the following code to load the data:

      superstore_sales_data_url = "/FileStore/tables/train-5.csv"  # Ensure this is the correct path
      df = spark.read.format("csv") \
                .option("header", "true") \
                .option("inferSchema", "true") \
                .load(superstore_sales_data_url)

Upload the Superstore dataset into Databricks.

Open the Databricks notebook and run the cells to perform data cleaning, transformation, and analysis.

** Usage **

## 2..Load the cleaned dataset:
  
  df = spark.read.format("delta").load("/FileStore/delta/superstore_cleaned")
  
 ## 3.Perform transformations, like calculating Profit Margin and extracting Order Month:

   from pyspark.sql.functions import col, month, year

  #Add Profit Margin column
  
  df_cleaned = df_cleaned.withColumn("Profit Margin", col("Profit") / col("Sales"))

  #Extract month and year from Order Date

  df_cleaned = df_cleaned.withColumn("Order_Month", month(col("Order_Date")))
  df_cleaned = df_cleaned.withColumn("Order_Year", year(col("Order_Date")))

### 4. Perform aggregations, such as total sales by category:

   total_sales_by_category = df_cleaned.groupBy("Category").agg(
      sum("Sales").alias("Total_Sales"),
      sum("Profit").alias("Total_Profit")
      )
   
###### 5. Save the results in a Delta table:

total_sales_by_category.write.format("delta").mode("overwrite").save("/FileStore/delta/total_sales_by_category")


##  Technologies Used  

1. Apache Spark (PySpark)
2. Delta Lake
3. Databricks (for execution environment)



