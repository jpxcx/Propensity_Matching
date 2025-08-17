# Propensity Score Matching Project 
**1. Data Cleaning & Preprocessing**
- Handled missing values and outliers
- Standardized variable formats and merged tables from PostgreSQL queries

**3. Exploratory Data Analysis (EDA)**
- Visualized buyer and seller behavior distributions
- Identified covariate imbalance between treatment and control groups

**4. Propensity Score Estimation**
- Implemented logistic regression and XGBoost models (scikit-learn, xgboost)
- Computed individual-level treatment probabilities (propensity scores)

**5. Matching & Evaluation**
- Matched treatment and control units using nearest-neighbor matching
- Assessed covariate balance post-matching
- Compared outcome variables to estimate treatment effects

**6. Key Results**
- Improved covariate balance after matching (bias reduced across major variables).
- Evidence of a measurable causal impact of the policy change on key buyer/seller metrics.
- XGBoost provided better separation and covariate balance compared to logistic regression in this dataset.
