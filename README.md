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
![SalePrice](https://user-images.githubusercontent.com/89664955/167196474-3d4d3ec8-1f08-45f9-98c8-245f59f7c0eb.JPG)
![LogSalePrice](https://user-images.githubusercontent.com/89664955/167196562-2810292d-b667-49d8-912f-e6035f4e8746.JPG)
![OverallQual](https://user-images.githubusercontent.com/89664955/167196664-6d0e0c69-e95e-4266-91ff-a633f5dcf2ad.JPG)

### Correlation with the log Sale Price:
![Numericalfeatures](https://user-images.githubusercontent.com/89664955/167196792-50a71a1e-08b0-484d-af76-52bfa0d3078a.JPG)

### Correlation matrix between the features:
![Correlation Table](https://user-images.githubusercontent.com/89664955/167196852-65226ccd-3ab9-4495-8bc8-81b4d4ca97d6.JPG)

### Performance Comparison (Metrics):
![ModelPerfomance](https://user-images.githubusercontent.com/89664955/167196943-6c248950-8dc9-419b-aca6-e48f0e60004c.JPG)

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
- Fill in missing values with 0's in the test set for a few features.
- IMPORTANT: When do label encoding, make sure that the test data and train data have the same number of features. Some of categorical features in test set don't contain all categories in the training set. 
- SOLUTION: Append extra rows with features containing missing categorical features to the dataframes so label encoding can produce the right amount of features.

#### Overview of the files in the repo:
- Data analysis.ipynb: File that analyzes the training dataset.
- Data outlook.ipynb: File that looks at all the raw features and see if there are no mismatch going on.
- Data model.ipynb: File that creates the models and train the models with the transformed train dataset.
- Transformed Train.csv: The training dataset that has been cleaned and label encoded with the target variable.
- Transformed Test.csv: The testing dataset that has been cleaned and label encoded, used to generate predicted prices.
- train.csv: Original training dataset.
- test.csv: Original testing dataset. 

#### Software Setup:
- pandas, matplotlib, sklearn, statsmodels, scipy stats.

#### Data/Citation:
- All the data is from GitHub.
- https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/data

