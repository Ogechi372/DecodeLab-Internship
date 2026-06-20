# DecodeLabs Internship Projects Portfolio

## Overview
This repository contains two data analysis projects completed 
using Microsoft Excel during my DecodeLabs internship. The 
projects focus on data cleaning, preparation, and exploratory 
data analysis (EDA) to generate meaningful insights from 
real-world sales datasets.

---

## Project 1: Data Cleaning and Preparation

### Project Description
The purpose of this project was to clean and prepare raw 
sales data for analysis using Microsoft Excel and Power Query. 
Several data quality issues such as duplicates, missing values, 
inconsistent formatting, and incorrect data types were 
identified and corrected.

### Objectives
- Improve overall data quality
- Remove duplicate records
- Handle missing values
- Standardize data formats
- Prepare the dataset for analysis and reporting

### Tools Used
- Microsoft Excel
- Power Query

### Dataset Information
Two real-world sales datasets containing 1,500 and 1,200 rows 
of business and operational records used for analytical 
reporting and data-driven decision-making.

### Data Cleaning Process
The following cleaning operations were performed using 
Power Query:
1. Removed duplicate rows
2. Handled missing values
3. Standardized text formatting
4. Changed incorrect data types
5. Renamed columns for consistency
6. Structured the dataset for analysis

---

## Messy Dataset
Initial raw dataset before cleaning and transformation.



![Messy Dataset](project_images1/messy_data.png)



---

### Power Query Techniques Used
- Remove Duplicates
- Replace Values
- Change Data Types
- Additional Columns
- Filtering and Sorting
- Data Transformation

### Power Query Transformation Steps
The following steps were applied in Power Query to clean 
and transform the dataset:

1. Connected to the raw Excel data source
2. Promoted first row as headers
3. Removed duplicate rows
4. Replaced missing/null values with appropriate defaults
5. Changed column data types to correct formats
6. Renamed columns for clarity and consistency
7. Removed irrelevant or empty columns
8. Filtered out invalid or erroneous records
9. Sorted data for better readability
10. Loaded cleaned data back into Excel

---

## Cleaned Dataset
Dataset after cleaning and preparation using Power Query.



![Cleaned Dataset](project_images1/clean_data.jpg)



---

### Challenges Faced
- Missing values across multiple columns
- Duplicate records affecting data integrity
- Inconsistent formatting
- Incorrect data types

### Outcome
The raw datasets were successfully transformed into clean, 
organized, and analysis-ready datasets suitable for reporting 
and further analysis.

---

## Project 2: Exploratory Data Analysis (EDA)

### Project Description
This project focuses on exploring and analyzing a sales 
dataset using Microsoft Excel to identify trends, patterns, 
relationships, and business insights.

### Objectives
- Analyze trends and patterns in the dataset
- Summarize data using descriptive statistics
- Perform quartile analysis to detect outliers
- Identify key performance observations

### Tools Used
- Microsoft Excel
- Pivot Tables
- Descriptive Statistics
- Quartile Calculations

### Analysis Performed
- Descriptive statistical analysis
- Monthly revenue analysis
- Order status analysis
- Outlier detection
- Revenue by payment method
- Quartile calculations

### Analytical Techniques Used
- Mean, Median, and Mode
- Minimum and Maximum Values
- Standard Deviation
- Quartile Analysis
- Frequency Distribution
- Pivot Table Summarization
- Data Filtering and Sorting

---

## Basic Descriptive Statistics
Summary statistics used to understand the dataset distribution.



![Basic Descriptive Statistics](project_images2/basic_descriptive_statistics.png)



---

## Monthly Revenue
Monthly revenue analysis to identify trends over time.



![Monthly Revenue](project_images2/monthly_revenue.png)



---

## Order Status
Distribution of order statuses across the dataset.



![Order Status](project_images2/order_status.png)



---

## Revenue by Products 
Revenue breakdown across different product categories.



![Revenue by Products](project_images2/revenue_by_product.png)



---

## Quartile Analysis
Quartile calculations used to identify data distribution 
and outliers. Outliers were detected based on total price 



![Quartile Analysis](project_images2/quartile_analysis.png)



---

### Key Insights
- Average order value was ₦1,053.97
- Chair and Printer were the top revenue-generating products
- Credit Card had the highest average spend at ₦1,127.55
- 8 orders were flagged as outliers above ₦3,330.41
- Order statuses were evenly distributed across all categories

### Challenges Faced
- Inconsistent formatting before analysis
- Organizing large volumes of data
- Data preparation before analysis

### Outcome
The exploratory data analysis provided meaningful insights 
and improved understanding of the dataset through statistical 
summaries and trend analysis.


# Project 3: SQL Data Analysis


---

## 📌 Project Overview

This project involves using **SQL (Structured Query Language)** to extract meaningful insights from a sales dataset. All queries were written and executed in **DB Browser for SQLite**.

Detail | Info |

 **Project** | Project 3 — SQL Data Analysis 
 
**Tool** | DB Browser for SQLite v3.13.1                        
 
**Database** | DecodeLab_Project3.db 
 
**Table** | Sales_Orders 
 
**Total Rows** | 1,200 
 
**Total Columns** | 14 
 
**Date Range** | January 2023 – June 2025

---

## 🎯 Project Goals

- Write **SELECT** queries to retrieve data
- Use **WHERE** to filter records
- Apply **ORDER BY** to sort results
- Perform aggregations using **COUNT**, **SUM**, and **AVG**
- Use **GROUP BY** to summarize data by category


## 📂 Dataset Description

The dataset is a **Sales Orders** table containing e-commerce transaction records with the following columns:

| Column | Description |
|--------|-------------|
| OrderID | Unique order identifier |
| Date | Date of order |
| CustomerID | Unique customer identifier |
| Product | Product purchased |
| Quantity | Number of items ordered |
| Unit Price | Price per unit |
| Shipping Address | Delivery address |
| Payment Method | Method of payment used |
| Order Status | Current status of order |
| Tracking Number | Shipment tracking number |
| Items-In-Cart | Number of items in cart |
| Coupon Code | Discount coupon applied |
| Referral Source | How customer found the store |
| Total Price | Final order value |

---

## 🛠️ Tools Used

- **DB Browser for SQLite v3.13.1** — SQL query editor and database management
- **Microsoft Excel** — Data cleaning and preparation (Projects 1 & 2)
- **SQLite** — Database engine

---

## 📝 SQL Queries

### Query 1 — View All Data (SELECT *)
```sql
SELECT * FROM Sales_Orders LIMIT 10;
```
**Purpose:** Preview the first 10 rows of the dataset to understand its structure.

---

### Query 2 — Select Specific Columns
```sql
SELECT OrderID, Product, "Total Price"
FROM Sales_Orders
LIMIT 10;
```
**Purpose:** Retrieve only relevant columns instead of all data.

---

### Query 3 — Filter by Product (WHERE)
```sql
SELECT * FROM Sales_Orders
WHERE Product = 'Chair';
```
**Purpose:** Filter all orders where the product is a Chair.
**Result:** 178 rows returned ✅

---

### Query 4 — Top 10 Highest Orders (ORDER BY)
```sql
SELECT OrderID, Product, "Total Price"
FROM Sales_Orders
ORDER BY "Total Price" DESC
LIMIT 10;
```
**Purpose:** Find the 10 highest value orders in the dataset.
**Result:** Orders ranged from ₦3,390.95 to #3,456.40

---

### Query 5 — Count Total Orders (COUNT)
```sql
SELECT COUNT(*) AS TotalOrders
FROM Sales_Orders;
```
**Purpose:** Count the total number of records in the table.
**Result:** 1,200 orders ✅

---

### Query 6 — Total Revenue (SUM)
```sql
SELECT SUM("Total Price") AS TotalRevenue
FROM Sales_Orders;
```
**Purpose:** Calculate the total revenue generated from all orders.
**Result:** ₦1,264,761.96 ✅

---

### Query 7 — Average Order Value (AVG)
```sql
SELECT AVG("Total Price") AS AvgOrderValue
FROM Sales_Orders;
```
**Purpose:** Calculate the average value of each order.
**Result:** ₦1,053.97 per order ✅

---

### Query 8 — Revenue by Product (GROUP BY)
```sql
SELECT Product, SUM("Total Price") AS Revenue
FROM Sales_Orders
GROUP BY Product
ORDER BY Revenue DESC;
```
**Purpose:** Find total revenue generated by each product.

**Result:**
| Product | Revenue (₦) 

 Chair | 195,620.11 
 Printer | 195,612.61 
 Laptop | 192,126.56 
 Tablet | 186,568.95 
 Monitor | 175,651.41 
 Desk | 167,459.93 
 Phone | 151,722.39 

---

### Query 9 — Order Status Distribution (GROUP BY)
```sql
SELECT "Order Status", COUNT(*) AS Count
FROM Sales_Orders
GROUP BY "Order Status"
ORDER BY Count DESC;
```
**Purpose:** Count how many orders fall under each status category.

**Result:**
 Order Status | Count 

 Cancelled | 250 
 Returned | 247 
 Pending | 237 
 Shipped | 235 
 Delivered | 231 

---

### Query 10 — Avg Spend by Payment Method (GROUP BY)
```sql
SELECT "Payment Method",
AVG("Total Price") AS AvgSpend
FROM Sales_Orders
GROUP BY "Payment Method"
ORDER BY AVG("Total Price") DESC;
```
**Purpose:** Find which payment method has the highest average order value.

**Result:**
| Payment Method | Avg Spend (₦) 

 Credit Card | 1,127.55 |
 Gift Card | 1,070.97 |
 Cash | 1,056.04 |
 Online | 1,017.22 |
 Debit Card | 1,001.56 |

---

## 📊 Key Findings

1. **Total Revenue** — ₦1,264,761.96 generated across all 1,200 orders
2. **Top Product** — Chair and Printer nearly tied at the top with ~₦195,000 each
3. **Cancellation Alert** — Cancelled orders (250) is the highest status category — more than Delivered (231). This needs business attention
4. **Best Payment Method** — Credit Card users spend the most on average (₦1,127.55 per order)
5. **Lowest Revenue Product** — Phone generates the least revenue (₦151,722.39)
6. **High Value Orders** — Top 10 orders all exceeded ₦3,300 — identified as legitimate large purchases



## Author
Umanta — Data Analytics Intern
