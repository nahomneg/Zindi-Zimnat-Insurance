# Zindi-Zimnat-Insurance

## Business Need
For insurance markets to work well, insurance companies need to be able to pool and spread
risk across a broad customer base. This works best where the population to be insured is diverse
and large. In Africa, formal insurance against risk has been hampered by lack of private sector
companies offering insurance, with no way to diversify and pool risk across populations.
Understanding the varied insurance needs of a population, and matching them to appropriate
products offered by insurance companies, makes insurance more effective and makes insurance
companies more successful.

## Objectives
For around 10,000 customers in the test set, all but one of the
products they own is given, and the model tries to make predictions around which products are most likely to
be the missing product. This same model can then be applied to any customer to identify
insurance products that might be useful to them given their current subscriptions.


## Data and Features
The data and feature description for this challenge can be found Here.

## Procedure
The test data has one of the products with a 1 entry changed to 0. 
That is, one of the subscribed products is given as unsubscribed.
Each row is duplicated as many times as the number of ones.
For each duplicated row in the training set one of the subscribed products is changed to unsubscribed.
A different product is changed from 1 to 0 on each duplicate of the row.
Now each row in the training set has one of the subscribed products missing, just like the test set. 

## Models Used
- Catboost Classifier with different parameters
- Random Forest with an n_estimator of 1000
- LGBM with n_estimators of 150, max_depth of 5 and num_leaves of 31
