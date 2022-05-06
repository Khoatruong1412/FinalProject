# FinalProject
### Overview:
House Prices - Advanced Regression Techniques
This repository holds an attempt to apply 3 different regression techniques: XGB, Random Forest, and AdaRegressor using the data from "House Prices - Advanced Regression Technique".

### Approach:
We use boxplots and anova to pick categorical features, and then we use correlation matrix to pick numerical features. Then, we compare the 3 different models and see which one performs best. XGB performs with the RMSE between predicted log prices: 0.1505.

### DATA:
- 1460 Training samples with 79 explanatory variables and 1 target variable (Sale Price). (train.csv)
- 1459 Testing samples with the same explanatory variables. (test.csv)
- Size of the whole data folder: 957.39 kB.

### Preprocessing / Clean up:
- Using ANOVA, boxplots, correlation matrix, and pandas to choose and clean up features.
- We only use 38 features with the same amount of training data.
- 75% of the data is training set, 25% of the data is testing test (Using the Transformed train.csv).

### Data visualization:

### Performance Comparison:
- RMSE between log prices:
+ XGB: 0.1505
+ Random Forest: 0.1528
+ AdaBoost: 0.2036

- RMSE Actual Prices:
+ XGB: 30352.2563
+ Random Forest: 29835.2760
+ AdaBoost: 38260.0632

- R2 Actual Prices:
+ XGB: 0.8685
+ Random Forest: 0.8729
+ AdaBoost: 0.7910

### Conclusion:
- Even though Random Forest has a higher R2, XGB achieved a better RMSE log price, the metric that the competition evaluates on.

### Future Work:
- Keep the target variables original and see if it performs better than log price.
- Some parts of the dwelling can strongly determine the price.

# How to reproduce the results above:
#### Instructions: 
- Import the training and testing sets with pandas.
- Plot all the boxplots for categorical features (The description text will let you know which one is categorical).
- Remove categorical features that have bad box plots and use one way ANOVA to choose your features.
- Use the correlation matrix to choose the numerical features.
- IMPORTANT: When do label encoding, make sure that the test data and train data have the same number of features. Some of categorical features in test set don't contain all categories in the training set. 
- SOLUTION: Append extra rows to the dataframes so label encoding can produce the right amount of features.

#### Software Setup:
- 
