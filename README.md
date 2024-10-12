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
7. [Results](#results)
8. [Conclusion](#conclusion)
9. [Future Work](#future-work)
10. [Usage](#usage)

## Introduction
This project analyzes car data from 2005, focusing on various characteristics to explore relationships with car prices. The analysis includes data manipulation, exploratory data analysis (EDA), and 2 stage regression modeling.

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

### Second Stage Regression
Use predicted prices from the first stage as a predictor in the second regression analysis, including additional categorical variables.

## Results
The regression results provide insights into how various factors influence car prices, indicating significant relationships between features like horsepower, fuel economy, and car categories.

## Conclusion
The analysis revealed key predictors of car prices and demonstrated the importance of considering multiple features in pricing models.

## Future Work
- Explore additional features or models to enhance prediction accuracy.
- Analyze trends over time using a larger dataset.
- Investigate the impact of external factors, such as economic conditions, on car pricing.

## Usage

To utilize the code for data analysis and modeling, follow the steps below:

### A. Import Required Libraries
Ensure you have the necessary libraries installed, such as Pandas, NumPy, Matplotlib, and Statsmodels.

### B. Load the Data
Load your dataset into a Pandas DataFrame to begin analysis.

### C. Data Exploration
Explore the structure of the DataFrame to understand the number of observations and columns.

### D. Data Processing and Feature Engineering
Add new features and categories based on the existing data, using functions and mappings as needed.

### E. Regression Modeling
Conduct regression analyses to predict car prices, starting with the first stage regression.

### F. Second Stage Regression
Use the predicted prices from the first stage in a second regression analysis.

This code provides a foundational approach to analyzing car pricing based on various features. You can modify the features or models as needed to enhance prediction accuracy.
