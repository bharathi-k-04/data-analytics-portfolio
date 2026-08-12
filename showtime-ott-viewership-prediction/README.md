# ShowTime OTT: Predicting First-Day Content Viewership

## Problem
ShowTime, an OTT streaming platform, wants to identify what drives first-day viewership for newly released content, in order to optimize release strategy, marketing spend, and scheduling decisions.

## Objective
- Identify the key factors that influence first-day content viewership
- Build a predictive model to estimate first-day views for future releases
- Translate findings into actionable release and marketing strategy

## Approach
- **Data**: 1,000 content releases across 8 variables (platform visitors, ad impressions, trailer views, genre, release day, season, sports-event overlap)
- **Preprocessing**: no missing values or duplicates; standardized categorical text fields, converted binary indicator to readable labels
- **EDA**: univariate and bivariate analysis, correlation heatmap, pairplots
- **Modeling**: Linear Regression, with categorical variables dummy-encoded; validated against multicollinearity (VIF), linearity, residual independence, normality (Shapiro-Wilk), and homoscedasticity assumptions

## Key Findings
- **Trailer views are the strongest predictor** — correlation of 0.75 with first-day views; ad impressions showed almost no correlation (~0.05)
- **Model performance**: R² = 0.79 (train) / 0.77 (test), MAPE ≈ 9% — strong fit with no signs of overfitting
- **Major sports events hurt viewership** — content released alongside major sporting events sees a significant, measurable drop
- **Release timing matters**: Wednesday, Saturday, and Sunday releases outperform other days; summer and winter releases outperform spring/fall
- **Platform traffic** (visitors) is a strong secondary driver of viewership

## Recommendations
- Prioritize trailer marketing investment — it's the single biggest lever on first-day views
- Avoid scheduling major releases against large sports events
- Release strategically on high-engagement days (Wed/Sat/Sun) and in high-engagement seasons
- Continue growing platform traffic through promotions, since it compounds with other factors

## Files
- `showtime_viewership_prediction.ipynb` — full analysis and modeling notebook
- `Business_Report_ShowTime.pdf` — written business report

## Tools
Python, pandas, NumPy, matplotlib, seaborn, statsmodels, scikit-learn
