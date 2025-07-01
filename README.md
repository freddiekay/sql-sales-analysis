# SQL Sales Analysis

This project uses SQL to explore a retail dataset and answer business questions related to revenue, sales trends, and product performance.

## Dataset

The dataset contains 1500 simulated sales transactions including:
- `OrderID`, `Date`, `Product`, `Category`, `Region`, `Quantity`, `UnitPrice`, `TotalSale`

## Key Business Questions & Queries

1. **Top 5 Products by Total Revenue**  
2. **Total Revenue by Region**  
3. **Monthly Sales Trends**  
4. **Unique Orders per Region**  
5. **Average Order Value**  
6. **Revenue by Category**

## Tools
- SQL (tested on SQLite & MySQL)
- DB Browser
- Dataset: `SQL_Sales_Data.csv`

## Insights
- The top-selling product was **Milk**
- The **Greater Accra** region generated the highest total revenue
- Revenue trends were tracked monthly from **January 2025 to May 2025**
- The highest revenue occurred in **March 2025** with **₵58,273.64**
- There were **1500 unique orders** distributed across 5 regions
- The **average order value** was approximately **₵174.88**
- Revenue by category showed strong performance in **Raw** and **Beverage** product types

## Sample SQL Query

```sql
SELECT Product, SUM(TotalSale) AS TotalRevenue
FROM sales_data
GROUP BY Product
ORDER BY TotalRevenue DESC
LIMIT 5;
