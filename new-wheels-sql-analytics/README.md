# New Wheels: Data Querying & Analytics with SQL

## Problem
New Wheels, a vehicle resale platform, has seen steadily declining sales, customer ratings, and new customer growth over the past year. The CEO needs a data-driven quarterly report answering strategic questions across customer distribution, vehicle preferences, satisfaction, and revenue to diagnose the decline.

## Objective
- Answer 10 leadership-level business questions using SQL against the transactional database
- Quantify the scale and drivers of the sales and satisfaction decline
- Translate query results into actionable business recommendations

## Approach
- **Data**: relational database (`customer_t`, `order_t`, `product_t`) covering 1,000 orders, 994 customers, FY2018
- **Method**: SQL — aggregations, joins, window functions (`RANK() OVER`, `LAG() OVER`), conditional aggregation, and quarter-over-quarter trend analysis across 10 business questions

## Key Findings
- **Shipping collapsed**: average delivery time rose from 57 days (Q1) to 174 days (Q4) — the single largest driver of the customer satisfaction crisis
- **Satisfaction cratered in lockstep**: average rating fell from 3.55 (Q1) to 2.40 (Q4); negative feedback surged from 22% to 60% of customers
- **Orders and revenue declined every quarter**: orders down 35.8% (310 → 199), net revenue down from ~$18M (Q1) to ~$8.6M (Q4)
- **Market concentration**: Texas and California jointly lead with 97 customers each; the top 5 states account for ~38% of the customer base
- **Chevrolet and Ford dominate** vehicle preference, with American brands taking all but one of the top 5 spots
- **Discount policy is narrow**: average discount by credit card type ranges only ~58–64%, suggesting limited differentiation

## Recommendations
- Treat shipping/logistics as the top priority — root-cause the Q3 delay spike and target sub-45-day delivery within two quarters
- Launch a customer satisfaction recovery plan (proactive outreach, service credits, real-time feedback loops) targeting a return to 3.50+ average rating
- Deepen investment in core states (Texas, California, Florida) while piloting expansion in underrepresented states
- Prioritize Chevrolet/Ford inventory given clear demand concentration
- Review discount structure — move toward tiered discounts tied to order value rather than uniform flat discounting

## Files
- `New_Wheels_SQL_Analytics_Report.pdf` — full written report with all 10 SQL questions, queries, outputs, and business recommendations
- `new_wheels_analysis_queries.sql` — all 10 SQL queries extracted as a standalone, runnable script

## Tools
SQL (joins, window functions, conditional aggregation)
