Notebooks info


Seller view:
Treatment is defined as take rate change >= 5% (can be tweaked if necessary)
From our definition of treatment and control, we can do propensity matching -> each treatment model is mapped to a control model
Seller sensitivity is defined as (treatment COGS change) - (control COGS change)

Take rate, COGS, ADO change is percent change, so a 50% increase in COGS change = March COGS * 1.5 = April COGS

XGBoost: AUC is ideally between 0.7 and 0.8, and the absolute difference between training AUC and holdout/validation AUC should be close to 0
AUC is greatly affected by outliers, and if COGS change = 0 rows are removed

How the get_comparable_pairs function works:
For a control model C to be matched to a treatment model T, the following must hold:
1. C is in the same gmv_bin and ado_bin as T. 
2. C must be the same join type (is_new_join column) as T
3. The difference between T's propensity score and C's propensity score is less than delta (a parameter of the function)

The pairing process went well if the percent of unmatched models is small and SMD is less than 0.2 for columns not correlated with the definition of treatment
(take_rate_march SMD is always large because it strongly correlates with take_rate_change)

Plots included:
Treatment definition (take_rate_change) distributions
Outcome definition (cogs_change) distributions
Seller sensitivity distribution
Seller sensitivity by COGS group
Seller sensitivity by seller type
Seller sensitivity by join type


Buyer view:
Treatment is defined as COGS change >= 5% (decided on after plotting distributions)
From our definition of treatment and control, we can do propensity matching -> each treatment model is mapped to a control model
Buyer sensitivity is defined as (treatment ADO change) - (control ADO change)

XGBoost: AUC is ideally between 0.7 and 0.8, and the absolute difference between training AUC and holdout/validation AUC should be close to 0
AUC is greatly affected by outliers, and if COGS change = 0 rows are removed

How the get_comparable_pairs function works:
For a control model C to be matched to a treatment model T, the following must hold:
1. C is in the same gmv_bin and ado_bin as T. 
2. C must be the same join type (is_new_join column) as T
3. The difference between T's propensity score and C's propensity score is less than delta (a parameter of the function)

The pairing process went well if the percent of unmatched models is small and SMD is less than 0.2 for columns not correlated with the definition of treatment

Plots included:
Treatment definition (cogs_change) distributions
Outcome definition (ado_change) distributions
Buyer sensitivity distribution
Buyer sensitivity by COGS group
Buyer sensitivity by seller type
Buyer sensitivity by join type


Query:
Some set-up needed for presto_password 
Put your SQL query in a string, do not include ";" at the end of the query or any comments in the query