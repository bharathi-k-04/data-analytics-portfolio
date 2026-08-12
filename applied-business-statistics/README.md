# Applied Business Statistics: Probability, Hypothesis Testing & ANOVA

## Overview
Four independent case studies applying core statistical methods to real business problems — probability, normal distribution analysis, hypothesis testing, and ANOVA — using Python (pandas, SciPy, statsmodels).

## Problem 1 — Probability: Sports Injury Risk
**Question**: What's the likelihood a player suffers a foot injury, and how does position affect that risk?
**Method**: Conditional probability
**Result**: ~62% overall injury probability; ~31% probability an injured player is specifically a striker.

## Problem 2 — Normal Distribution: Quality Control
**Question**: What proportion of packaging bags fall outside acceptable breaking-strength tolerances?
**Method**: Normal distribution / z-scores
**Result**: Only ~11% of bags fall below the minimum strength threshold — used to quantify defect rate for the supply chain.

## Problem 3 — Hypothesis Testing: Material Suitability
**Question**: Are unpolished stones hard enough for printing, and does polishing significantly change hardness?
**Method**: Two-sample t-tests (5% significance)
**Result**: Unpolished stones are significantly softer than required (p = 0.0001) — unsuitable for printing; polished vs. unpolished hardness differs significantly (p = 0.0016).

## Problem 4 — ANOVA: Manufacturing Process Factors
**Question**: Does implant hardness depend more on the dentist or the method used?
**Method**: One-way & two-way ANOVA, with Shapiro-Wilk/Levene checks and Tukey HSD post-hoc tests
**Result**: Dentist alone has no significant effect (p > 0.11); implant **method** does (p = 0.004, p < 0.001) — method is the dominant, controllable factor, not the individual practitioner.

## Files
- `applied_business_statistics.ipynb` — full analysis notebook
- `Applied_Business_Statistics_Report.pdf` — written report

## Tools
Python, pandas, NumPy, SciPy, statsmodels
