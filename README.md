# Blinkit Sales and Performance Analysis Using SQL

## Overview
This project focuses on analyzing Blinkit's sales performance, customer satisfaction, and inventory distribution using SQL. The goal is to identify key insights and opportunities for optimization by querying and analyzing the dataset. The project provides actionable insights to improve business operations and decision-making.

## Business Requirements
The primary objectives of this analysis are:
1. **Sales Performance Analysis**: Evaluate total sales, average sales, and sales distribution across different outlets, item types, and locations.
2. **Customer Satisfaction**: Analyze average ratings and their correlation with sales and other KPIs.
3. **Inventory Distribution**: Assess the impact of fat content and outlet size on sales performance.
4. **Outlet Performance**: Compare sales and other metrics across different outlet types, sizes, and locations.

## Key Performance Indicators (KPIs)
The following KPIs were analyzed:
- **Total Sales**
- **Average Sales**
- **Number of Items Sold**
- **Average Rating**
- **Sales by Outlet Size**
- **Sales by Outlet Location**
- **Sales by Outlet Type**

## Granular Requirements and Objectives
### 1. Impact of Fat Content on Sales
   - **Objective**: Analyze how fat content influences total sales.
   - **Additional KPIs**: Average Sales, Number of Items, Average Rating.

### 2. Performance of Different Item Types
   - **Objective**: Identify the performance of various item types in terms of total sales.
   - **Additional KPIs**: Average Sales, Number of Items, Average Rating.

### 3. Sales Comparison Across Outlets
   - **Objective**: Compare total sales across different outlets segmented by fat content.
   - **Additional KPIs**: Average Sales, Number of Items, Average Rating.

### 4. Influence of Outlet Age/Type on Sales
   - **Objective**: Evaluate how the age or type of outlet establishment influences total sales.

### 5. Percentage of Sales by Outlet Size
   - **Objective**: Analyze the correlation between outlet size and total sales.

### 6. Sales by Outlet Location
   - **Objective**: Assess the geographic distribution of sales across different locations.

### 7. All Metrics by Outlet Type
   - **Objective**: Provide a comprehensive view of all key metrics (Total Sales, Average Sales, Number of Items, Average Rating) broken down by different outlet types.

## Tools and Technologies
- **SQL**: For querying and analyzing the dataset.
- **Database**: MySQL (or any other relational database you used).

## Dataset
The dataset includes the following key tables:
- **Sales Data**: Contains information on total sales, average sales, and number of items sold.
- **Customer Ratings**: Includes average ratings for products and outlets.
- **Outlet Information**: Details about outlet size, location, type, and establishment age.
- **Product Information**: Includes product types and fat content.

## SQL Queries
Here are some examples of SQL queries used in the analysis:
```sql
-- Query to analyze sales by outlet type
SELECT outlet_type, SUM(total_sales) AS total_sales
FROM sales_data
GROUP BY outlet_type;

-- Query to evaluate the impact of fat content on sales
SELECT fat_content, SUM(total_sales) AS total_sales, AVG(average_sales) AS avg_sales
FROM sales_data
GROUP BY fat_content;

-- Query to compare sales across different locations
SELECT outlet_location, SUM(total_sales) AS total_sales
FROM sales_data
GROUP BY outlet_location;

-- Query to analyze sales by outlet size
SELECT outlet_size, SUM(total_sales) AS total_sales
FROM sales_data
GROUP BY outlet_size;

