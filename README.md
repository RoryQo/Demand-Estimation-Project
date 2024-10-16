# Project README

## Table of Contents
1. [Introduction](#introduction)
2. [Requirements](#requirements)
3. [Data Overview](#data-overview) 
4. [Data Processing](#data-processing)
   - [Loading Data](#loading-data)
   - [Data Cleaning](#data-cleaning)
   - [Feature Engineering](#feature-engineering)
5. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
   - [Descriptive Statistics](#descriptive-statistics)
   - [Visualizations](#visualizations)
6. [Modeling](#modeling)
   - [First Stage Regression](#first-stage-regression)
   - [Second Stage Regression](#second-stage-regression)
7. [Future Work](#future-work)
8. [Results Analysis](#results-analysis)

## Introduction
This project analyzes car data from 2005, focusing on various characteristics to explore relationships with car prices. The analysis includes data manipulation, exploratory data analysis (EDA), and regression modeling.

## Requirements
- Python 3.x
- Pandas
- NumPy
- Matplotlib
- Statsmodels

## Data Overview
The dataset consists of 217 observations across 18 columns, including features such as year, manufacturer, model, and various performance metrics (e.g., horsepower, fuel economy).

## Data Processing

### Loading Data
Load the dataset into a Pandas DataFrame.

### Data Cleaning
Inspect the data structure and identify any necessary cleaning.

### Feature Engineering
- **Categorization:** Create car categories based on segmentation.
- **Derived Features:** Calculate combined MPG and footprint metrics.

## Exploratory Data Analysis (EDA)

### Descriptive Statistics
Obtain summary statistics to understand data distribution.

### Visualizations
- Create boxplots to compare fuel economy across manufacturers.
- Generate bar plots for quantity sold by car category.
- Use scatter plots to explore relationships between price and quantity.

<div style="display: flex; justify-content: space-around;">
    <img src="https://github.com/RoryQo/Demand-Estimation-Project/raw/main/Graph1.jpg" alt="Graph 1" style="width: 400px;"/>
    <img src="https://github.com/RoryQo/Demand-Estimation-Project/raw/main/graph2.jpg" alt="Graph 2" style="width: 400px;"/>
</div>

## Modeling

### First Stage Regression
Conduct a regression analysis to predict car prices based on selected features.

```
firstStageV1 = smf.ols(formula='Price ~   hp + mpg_combined + footprint + hpDist + mpg_combinedDist + footprintDist',data=df).fit(cov_type='HC1')
```

### Second Stage Regression
The original regression equation is estimated, replacing the endogenous variable with its predicted values from the first stage. This helps to provide a more accurate estimate of the coefficients since the endogeneity issue has been addressed.

## Future Work
- Explore additional features or models to enhance prediction accuracy.
- Analyze trends over time using a larger dataset.
- Investigate the impact of external factors, such as economic conditions, on car pricing.

## Results Analysis
The two-stage regression approach provided valuable insights into the factors affecting car prices:

1. **First Stage Regression Results:**
   - The Adjusted R-squared of approximately 0.58 indicates that about 58% of the variability in car prices can be explained by the model, suggesting some predictive power but room for improvement.

2. **Second Stage Regression Results:**
   - The Adjusted R-squared increased to around 0.63, indicating an improvement in the model's explanatory power. This suggests that additional variables contribute to explaining more of the variation in car prices.

### Key Insights:
- **Impact of Features:** 
  - A negative coefficient for combined MPG suggests higher fuel efficiency may be associated with lower prices, which could warrant further investigation.
  - Statistical significance (p-values) highlights which variables meaningfully relate to car prices.

- **Interpreting Coefficients:**
  - Each coefficient reflects the expected change in car price for a one-unit increase in the predictor variable, holding others constant.

### Conclusion:
The two-stage regression results illuminate key predictors of car prices while addressing endogeneity, reflecting the importance of incorporating predicted values to enhance model performance.
