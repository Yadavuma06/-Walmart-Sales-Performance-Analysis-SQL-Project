# 📊 Walmart-Sales-Performance-Analysis-SQL-Project
This project demonstrates a data-driven sales analysis of Walmart stores using SQL. It applies real-world data analytics techniques to uncover insights into store performance, customer behavior, and category-wise sales trends — all using pure SQL. 


## 🎯 Objectives

* Evaluate branch performance and sales growth

* Identify high-revenue product categories

* Analyze seasonal and monthly sales trends

* Understand customer purchase frequency and patterns

* Derive business recommendations using SQL analytics

## 🧩 Dataset Overview

* Source: Walmart Sales transactional dataset

* Columns include: Invoice ID, Branch, City, Customer Type, Gender, Product Line, Unit Price, Quantity, Tax, Total, Date, Time, Payment, COGS, Gross Margin %, Rating

## ⚙️ Methods & Techniques Used

| Technique / Method | Description |
|--------------------|-------------|
| **Data Cleaning** | Removed nulls, duplicates, and inconsistent entries to ensure data accuracy. |
| **Data Filtering** | Used `WHERE`, `GROUP BY`, and `HAVING` clauses to extract meaningful subsets. |
| **Aggregation Functions** | Applied `SUM()`, `AVG()`, `COUNT()`, and `MAX()` for summarizing performance metrics. |
| **Joins & Subqueries** | Combined multiple tables using `INNER JOIN` and `LEFT JOIN` for cross-sectional analysis. |
| **Window Functions** | Used `RANK()`, `ROW_NUMBER()`, and `OVER()` for ranking and comparative analysis. |
| **Date & Time Functions** | Extracted and grouped sales by month, day, and time for trend identification. |
| **CTEs (Common Table Expressions)** | Simplified complex queries and improved readability. |
| **Case Statements** | Applied conditional logic to categorize or segment data dynamically. |
| **Performance Optimization** | Ensured efficient query execution through proper indexing and filtering. |


## 📁 Project Structure

| File | Description |
|------|-------------|
| `Task1.sql` | Branch-wise sales growth analysis |
| `Task2.sql` | Monthly and seasonal trend analysis |
| `Task3.sql` | Category-wise revenue and profitability |
| `Task4.sql` | Peak shopping hours & day analysis |
| `Task5.sql` | Customer segmentation |
| `Task6.sql` | Payment type preferences |
| `Task7.sql` | Gender-based spending pattern |
| `Task8.sql` | Branch comparison dashboard |
| `Sales Performance Analysis of Walmart Stores.pptx` | Summary presentation with insights & visuals |



## 📈 Key Insights

* Branch C showed the highest sales growth percentage across months.

* Electronics & Food categories dominated revenue share.

* Evening hours (5–8 PM) had the highest customer traffic.

* Credit card payments were most frequent among high spenders.

* Female customers had a slightly higher average purchase total. 

## 💡 Sample Query: Branch Growth

```sql
SELECT branch,
       ROUND((MAX(total)-MIN(total))/MIN(total)*100,2) AS Sales_growth
FROM (
      SELECT branch,
             DATE_FORMAT(STR_TO_DATE(Date,'%d-%m-%Y'), '%Y-%m') AS month,
             SUM(total) AS Total
      FROM Walmartsales
      GROUP BY Branch, month
     ) AS monthly_data
GROUP BY Branch
ORDER BY Sales_growth DESC
LIMIT 1;

```

## 🚀 Outcome

This project enhanced my ability to:

* Write optimized, modular SQL queries

* Clean and transform time-based datasets

* Extract actionable business insights from raw data

* Communicate findings through concise visualization and storytelling

## 👨‍💻 Author

Uma Yadav
📈 Aspiring Data Analyst | SQL Enthusiast

[🔗 LinkedIn Profile]([https://your-link-here.com](https://www.linkedin.com/in/uma-yadav6/))

