# Credit Card Customer Segmentation: AllLife Bank

## Problem
AllLife Bank wants to improve market penetration through personalized marketing and address poor customer support by upgrading its service delivery model. Both goals require understanding who their credit card customers actually are, beyond a one-size-fits-all approach.

## Objective
- Apply unsupervised learning to segment customers into distinct, meaningful groups based on financial attributes and interaction behavior
- Profile each segment's defining characteristics, size, and business significance
- Deliver segment-specific recommendations for both Marketing and Operations

## Approach
- **Data**: 660 customers, 5 clustering features (average credit limit, total credit cards, bank visits, online visits, calls made)
- **Preprocessing**: no missing values; retained legitimate outliers (premium/HNI customers, highly digital users) rather than removing them; applied StandardScaler before clustering
- **Modeling**: K-Means (Elbow Method + Silhouette Score) and Hierarchical Clustering (Cophenetic Correlation + dendrograms), cross-validated against each other

## Key Findings
- **Both methods independently converge on 3 clusters** as optimal, with near-perfect agreement between them (Adjusted Rand Index = 0.9944) — strong validation of the segmentation
- **Mid-Value, Branch-Preferring (58% of customers)**: moderate credit limit, highest branch visits, almost no online activity
- **Low-Value, Call-Heavy (34% of customers)**: lowest credit limit and card count, by far the highest call volume — the main driver of call center load and likely service dissatisfaction
- **High-Value, Digital-First (8% of customers)**: highest credit limit (~₹1.4L) and card count, almost entirely digital, rarely calls or visits — the bank's premium segment

## Recommendations
- **Low-Value, Call-Heavy segment**: prioritize for the service delivery upgrade — proactive outreach, self-service/IVR tools, and dedicated support to cut call volume and improve satisfaction
- **Mid-Value, Branch-Preferring segment**: in-branch personalized offers and relationship manager engagement, with a phased digital-adoption push
- **High-Value, Digital-First segment**: premium card upsells, exclusive digital features, and a robust digital platform — this segment carries the highest per-customer ROI and highest churn risk if service quality slips
- Re-run segmentation quarterly/semi-annually to track customer migration between segments and measure the impact of service changes

## Files
- `credit_card_customer_segmentation.ipynb` — full analysis and clustering notebook
- `Business_Report_Credit_Card_Segmentation.pdf` — written business report

## Tools
Python, pandas, NumPy, matplotlib, seaborn, scikit-learn, SciPy
