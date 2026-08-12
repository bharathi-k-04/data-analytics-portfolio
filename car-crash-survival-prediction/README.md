# Car Crash Survival Prediction: Classification Modeling for Road Safety

## Problem
The Department of Road Transport has seen a 15% year-over-year rise in urban car crashes and wants to move from reactive (post-crash) analysis to proactive risk prediction — identifying which factors most influence survival, to inform road-safety policy.

## Objective
- Analyze historical crash data to uncover patterns in occupant survival
- Build a classification model to predict likelihood of survival in a crash
- Identify the most critical, actionable factors driving fatality risk

## Approach
- **Data**: 11,217 crash records across 12 variables (speed, seatbelt use, airbag status, impact type, occupant age/sex/role, vehicle age)
- **Key challenge**: heavily imbalanced target (~89.5% survived vs. ~10.5% deceased) — **Recall** chosen as the primary metric, since missing a true fatality risk (false negative) is far costlier than a false alarm in a safety context
- **Modeling**: Logistic Regression and Decision Tree, each in base and tuned form (threshold optimization via ROC/Youden's J for Logistic Regression; pre-pruning via GridSearchCV for Decision Tree)
- **Feature engineering**: derived vehicle age at time of crash (`veh_usage_duration`) from model year and accident year

## Key Findings
- **Speed is the dominant fatality predictor** — crashes at 55+ km/h show dramatically higher mortality than low-speed impacts
- **Seatbelt non-use significantly elevates risk** — ~30% of occupants were unbelted, a major contributor to fatality
- **Airbag *unavailability*, not just non-deployment, is the bigger gap** — over 37% of crashes involved vehicles with no airbag present at all
- **Compounding effect**: no seatbelt + no airbag together produces the highest fatality rate in the dataset
- **Elderly occupants (60+) face disproportionately high risk**, with fatality rate rising steadily with age
- **Final model**: a pre-pruned Decision Tree, chosen for its balance of recall and generalizability, and for producing transparent, rule-based explanations regulators can act on directly

## Recommendations
- Mandate airbag installation in all new and resale vehicles
- Deploy automated speed enforcement in high-risk urban corridors
- Introduce camera-based seatbelt compliance enforcement
- Require periodic safety inspections for vehicles over 10 years old
- Launch targeted safety programs for elderly drivers and behavioral campaigns for male drivers (higher risk-taking correlation)
- For future modeling: address class imbalance with SMOTE or cost-sensitive learning, and collect richer features (weather, road type, alcohol involvement)

## Files
- `car_crash_survival_prediction.ipynb` — full analysis and modeling notebook
- `Business_Report_Car_Crash_Classification.pdf` — written business report

## Tools
Python, pandas, NumPy, matplotlib, seaborn, scikit-learn, statsmodels
