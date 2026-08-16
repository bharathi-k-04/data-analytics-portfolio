Walmart Sales Data Analysis (SQL)
Problem

Analyze Walmart branch-level sales transaction data to uncover patterns in payment behavior, product category performance, sales timing, and revenue trends across branches and cities.

Objective

Answer 9 business questions using SQL against a Walmart sales transactions dataset, covering payment methods, category performance, sales timing, and branch-level revenue trends.

Approach
Tool: SQL (MySQL)
Techniques: aggregations (COUNT, SUM, AVG, MIN, MAX), window functions (RANK() OVER PARTITION BY), CTEs, CASE-based time-shift categorization, and a self-join for year-over-year revenue comparison
Business Questions Answered
Payment method distribution — transactions and quantity sold per method
Highest-rated product category per branch
Busiest day of the week per branch
Total quantity sold per payment method
Min/max/avg rating per category per city
Total profit per category
Most common (preferred) payment method per branch
Sales distribution across Morning/Afternoon/Evening shifts
Top 5 branches by year-over-year revenue decline
Files
walmart_sales_analysis_queries.sql — all 9 SQL queries
Tools

SQL (MySQL)
