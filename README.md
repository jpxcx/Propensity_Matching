# Propensity Score Matching Project 
Methods
1. Data Cleaning & Preprocessing

Handled missing values and outliers

Standardized variable formats and merged tables from PostgreSQL queries

3. Exploratory Data Analysis (EDA)
Visualized buyer and seller behavior distributions
Identified covariate imbalance between treatment and control groups

4. Propensity Score Estimation
Implemented logistic regression and XGBoost models (scikit-learn, xgboost)
Computed individual-level treatment probabilities (propensity scores)

5. Matching & Evaluation
Matched treatment and control units using nearest-neighbor matching
Assessed covariate balance post-matching
Compared outcome variables to estimate treatment effects
