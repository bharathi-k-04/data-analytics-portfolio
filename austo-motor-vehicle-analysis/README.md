# Austo Motor Company: Vehicle Preference & Marketing Strategy Analysis

## Problem
Austo Motor Company's board raised concerns about the efficiency of its marketing campaigns and how well they align with customer preferences. This project analyzes customer and purchase data to uncover patterns and provide actionable recommendations for marketing and sales strategy.

## Objective
- Assess how profession, gender, age, and household income influence vehicle choice and price
- Evaluate the impact of loans and dual-income households on spending patterns
- Deliver actionable insights for targeted marketing, product positioning, and sales optimization

## Approach
- **Data**: 1,581 customer records across 14 variables (demographics, income, loan status, vehicle type & price)
- **Cleaning**: fixed inconsistent category labels, imputed missing gender (mode) and partner salary (median, to handle right-skew), checked for duplicates
- **Analysis**: Exploratory Data Analysis (EDA) — univariate, bivariate, and multivariate exploration using Python (pandas, matplotlib, seaborn)

## Key Findings
- **Gender is a strong signal**: 52%+ of female customers buy SUVs vs. under 10% of male customers, who lean toward hatchbacks and sedans
- **Female customers spend more per vehicle**: median price $49,000 vs. $29,000 for male customers — a premium-segment opportunity
- **Vehicle type is the strongest price driver**: hatchback median $27,000 → SUV median $57,000
- **Life stage matters more than gender alone**: SUV adoption begins in the late 20s and dominates after 30, peaking in the 36–45 age group
- **Loans and partner income**: personal loan status doesn't drive premium purchases; a working partner alone doesn't raise spend, but partner *salary* correlates with higher-priced (often SUV) purchases

## Recommendations
- Gender-targeted premium campaigns (SUVs to female customers)
- Age/life-stage-based product positioning
- Income-tier pricing and promotion strategy

## Files
- `austo_motor_vehicle_analysis.ipynb` — full analysis notebook
- `Business_Report_Austo_Motor.pdf` — written business report

## Tools
Python, pandas, NumPy, matplotlib, seaborn
