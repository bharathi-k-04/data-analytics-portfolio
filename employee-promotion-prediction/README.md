# Employee Promotion Prediction: A Classification Study for JMD Company

## Problem
JMD Company's HR team manually compares employee attributes each promotion cycle, causing delays and inconsistent decisions. The company wants a data-driven system to identify promotion-worthy employees faster and more consistently.

## Objective
- Predict which employees are likely to be promoted, using historical HR data
- Identify the strongest drivers of promotion to inform HR policy
- Provide a precision-oriented shortlisting tool for HR decision-making

## Approach
- **Data**: 54,808 employee records, 13 attributes (training scores, ratings, awards, department, education, tenure, etc.)
- **Key challenge**: severe class imbalance (~91.5% not promoted vs. ~8.5% promoted) — addressed by comparing original, SMOTE-oversampled, and undersampled training data
- **Modeling**: five ensemble classifiers (Decision Tree, Random Forest, Bagging, AdaBoost, Gradient Boosting) evaluated via stratified train/validation/test splits; F1-macro chosen as the primary metric to balance false positives (wasted promotions) against false negatives (lost talent)
- **Tuning**: hyperparameter tuning applied to the top 3 candidate model/data combinations

## Key Findings
- **Average training score is the single strongest predictor** (~52% of the final model's importance) — a clear signal that performance evaluation drives promotion outcomes
- **Award winners are ~3x more likely to be promoted** (~22–25% vs. ~8.5% base rate), despite only ~4% of employees winning one
- **Past performance rating compounds**: employees rated 4–5 have 14–19% promotion rates vs. under 1% for ratings 1–2
- **Referral hires promote at nearly 2x the rate** of sourced hires (~14% vs. ~8.7%)
- **No meaningful gender gap** in historical promotion rates (male ~8.8% vs. female ~8.0%)
- **Final model**: Tuned Gradient Boosting on original (non-resampled) data — test F1-macro ≈ 0.729, accuracy ≈ 94%, precision ≈ 91%, recall ≈ 33% — a conservative, high-precision shortlisting tool

## Recommendations
- Set a minimum training-score threshold (~70+) as an entry condition for the promotion pipeline
- Use the model as a shortlisting tool for HR review, not a final decision-maker
- Strengthen and expand the award recognition program, which strongly correlates with genuine high performers
- Move toward department-adjusted promotion criteria instead of a single company-wide bar
- Flag high-rating, high-training-score employees who weren't promoted as retention/attrition risks
- Re-evaluate the "number of trainings" policy, since training *count* has near-zero predictive value compared to training *score*

## Files
- `employee_promotion_prediction.ipynb` — full analysis and modeling notebook
- `Business_Report_Employee_Promotion.pdf` — written business report

## Tools
Python, pandas, NumPy, matplotlib, seaborn, scikit-learn, imbalanced-learn (SMOTE)
