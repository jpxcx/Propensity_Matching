# Propensity Score Matching Project 
##Project Overview

This project evaluates the causal impact of a policy change on Shopee buyers and sellers using propensity score matching (PSM).
By matching treatment and control groups on observable characteristics, we reduce selection bias and estimate the true effect of the intervention.

The work is based on my Summer 2025 Data Science Internship at Shopee and has been refactored for open-source demonstration.

**Methods**
1. Data Cleaning & Preprocessing
- Handled missing values and outliers
- Standardized variable formats and merged tables from PostgreSQL queries

2. Exploratory Data Analysis (EDA)
- Visualized buyer and seller behavior distributions
- Identified covariate imbalance between treatment and control groups

3. Propensity Score Estimation
- Implemented logistic regression and XGBoost models (scikit-learn, xgboost)
- Computed individual-level treatment probabilities (propensity scores)

4. Matching & Evaluation
- Matched treatment and control units using nearest-neighbor matching
- Assessed covariate balance post-matching
- Compared outcome variables to estimate treatment effects

**Key Results**
- Improved covariate balance after matching (bias reduced across major variables).
- Evidence of a measurable causal impact of the policy change on key buyer/seller metrics.
- XGBoost provided better separation and covariate balance compared to logistic regression in this dataset.
