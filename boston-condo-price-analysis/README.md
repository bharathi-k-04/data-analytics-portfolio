# Boston Condo Analysis: Pricing Drivers for a Recommendation System

## Problem
Understand what actually drives condo sale prices in Boston — location, size, bed/bath configuration, tax burden, and commercial proximity — to inform a property recommendation system with neighborhood-aware pricing logic rather than a one-size-fits-all model.

## Objective
Answer five key questions from the sales data:
- How are sale prices distributed across the market?
- What bed/bath combinations dominate by neighborhood?
- How well does square footage predict price?
- How concentrated is the property tax burden by street?
- Does proximity to small commercial establishments (RC) affect price?

## Approach
- **Tool**: Tableau — 10 worksheets combined into a 5-dashboard storyboard (bubble charts, box plots, histograms, heatmaps, scatter plots)
- **Method**: descriptive and correlation analysis across sale price, square footage, bed/bath counts, property tax, and commercial-proximity flag (RC), broken out by neighborhood and street

## Key Findings
- **Price distribution**: right-skewed — nearly 90% of sales are under $225K; Neighborhood "E" is a distinct luxury outlier with sales up to $900K+
- **Bed/bath mix**: 2-bed/1-bath is the dominant product type (142 sales, nearly double any other combination) — a standardized "starter condo" profile
- **Size vs. price**: moderate positive correlation (R² = 0.48) — square footage matters, but isn't sufficient alone (e.g., a ~1,900 sqft unit sold under $250K)
- **Tax concentration**: property tax burden is concentrated in ~15 premium streets, led by Cambridge Pkwy ($3,672 avg — 30%+ higher than the next-highest street)
- **Commercial proximity hurts, not helps**: properties *without* nearby small commercial establishments (RC=0) sell for ~26% more on average ($200K vs. $149K) — likely a preference for quieter residential settings

## Recommendations
- Treat Neighborhood E as a distinct premium tier with its own pricing pathway in the recommendation engine
- Prioritize 2-bed/1-bath inventory sourcing and matching, since it serves the largest buyer segment
- Combine square footage with bed/bath and area in the pricing model rather than relying on square footage alone
- Flag high-tax streets explicitly in listings to set buyer expectations upfront
- Don't assume commercial proximity adds value — apply neighborhood-specific pricing rules instead of one uniform model across Boston

## Live Dashboard
Interactive version on Tableau Public: [Boston Condo Analysis Storyboard](https://public.tableau.com/app/profile/bharathi.k1055/viz/BostonCondoAnalysis_17856916997730/BostonCondoAnalysisStoryboard)

## Files
- `Boston_Condo_Analysis.twbx` — packaged Tableau workbook (open in Tableau Desktop or Tableau Public)

## Tools
Tableau
