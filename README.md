# Project Name
> Housing Price Assignment : To predict the prices of the houses in Australia and sell it on a higher price


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)



## General Information
- A US company wants to enter into the Real Estate market in Australia. It wants to predict the houses in Australia, knowing the prices it would try to quote the prices of the house in a higher side. For this the company want to select the house properties to buy that are in more preferable for people to buy.

### Objective
- To build a regression model using regularisation in order to predict the actual value of the prospective properties and decide whether to invest in them or not.
- The company wants to know:
    - Which variables are significant in predicting the price of a house, and
    - How well those variables describe the price of a house.


### Acceptance Criteria

- Build a regression model using all the variables
- Apply regularization techniques - Ridge and Lasso
- Determine the optimal value of lambda for Ridge and Lasso

### Data
- The data is provided in the csv file format.
- Training data is provided



## Technologies Used
    - numpy 1.23.5
    - pandas 1.5.2
    - seaborn 0.12.1
    - matplotlib 3.6.2
    - sklearn 1.2.1


## Conclusions
- Insights post Data Cleaning
    - No null values present in any columns
    - Header and Footer rows are fine
    - All Columns have column header
    - Dropped the column Id as it is kind of rudundant - storing only the sequence and will not contribute anything in the analysis
    - Columns PoolQC, MiscFeature are dropped due to high null value content
    - Data types of both categorical and numerical are converted accordingly
- Insight on Univariate Analysis
    - Numerical Column insights
        1. Null values has been replaced by 0
        2. Histogram plots and box plots are plotted for analysis
        3. Around 23 columns are identified as numerical
    - Categorical columns insights
        1. 55 columns were under the categorical
        2. Count plot is plotted for analysis
    - Outliers
        1. Few outliers are observed
        2. Nearly 50 rows are removed as part of outliers
- Insight on Bivariate Analysis
    - Barplot and box plots are plotted against column salePrice
    - Scatter plot are created with target column SalePrice
    - Distribution plot are done for year columns
- Insights on Co-rrelation variables in the data set
    - Correlation is detected using heat map
    - Quite a few columns are highly correlated
    - Milti-collinearity is detected and columns are dropped having a high correlation above 0.7
- Data Preparation
    1. Creation of Dummy Variables for the categorical fields
- MODEL building
    1. Spliting X and y
    2. Scaling the features
    - Model - A : 
        1. Taking all the features and building a Linaer model
        2. Applying Ridge and Lasso regularization
        3. Comparing the metrics
    - Model - B1
        1. Applying RFE and removing the features having high VIF values
        2. Applying Ridge and Lasso regularization
        3. Comparing the metrics
    - Model - B2
        1. Applying RFE and taking 150 columns as feature selection
        2. Applying Ridge and Lasso regularization
        3. Comparing the metrics
    - Model - B3
        1. Applying RFE and taking 50 columns as feature selection
        2. Applying Ridge and Lasso regularization
        3. Comparing the metrics

- Final Insights
    1. Model - A seems to have a good model among all
    2. Lasso regression is better as compared to Ridge
    3. Lasso perfoms nearly similar both in train and test data set
    4. Optimal alpha value for Lasso came to be 100

## Contact
Created by Sagar Sahoo


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->