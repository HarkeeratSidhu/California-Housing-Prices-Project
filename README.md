California Housing Prices Analysis
This repository contains an analysis of the California Housing Prices dataset, using various statistical and machine learning methods. The dataset, derived from the 1990 Census, includes information such as median house prices, location data, and demographic details for California districts.

Table of Contents
Introduction
Data Overview
Data Cleaning and Preparation
Exploratory Data Analysis
Modeling
Results
Conclusion
References
Introduction
This project aims to:

Predict housing prices based on demographic and geographical factors.
Classify districts based on their proximity to the ocean.
Note: While the dataset is outdated, it provides a valuable foundation for practicing data science techniques.

Data Overview
The dataset consists of the following columns:

longitude and latitude: Geographical location of districts.
housing_median_age: Median age of houses.
total_rooms and total_bedrooms: Number of rooms and bedrooms per block.
population and households: Demographic information.
median_income: Median income per block.
median_house_value: Median house price (capped at $500,001).
ocean_proximity: Proximity to ocean categories.
Data Cleaning and Preparation
Steps:
Handling Missing Values:
Missing values in total_bedrooms were imputed using stochastic regression to preserve distribution and correlations.
Outliers:
Removed entries with capped median_house_value to avoid skewing results.
Final Dataset:
Combined cleaned data frames for further analysis.
Exploratory Data Analysis
Histograms and visualizations revealed key patterns in income, housing age, and proximity to the ocean.
Outlier analysis confirmed capped values in house prices and significant variation in high-value housing.
Modeling
1. Cluster Analysis
Used the k-prototype algorithm to group districts into clusters.
Optimal clusters determined using the elbow rule and silhouette widths.
2. Multinomial Regression
Predicted ocean_proximity with 80% accuracy.
Struggled with minority classes (e.g., island homes).
3. Linear Regression
Modeled median_house_value against other variables.
Adjusted R-squared improved with log transformations, but normality and variance assumptions were violated.
4. Random Forest Regression
Achieved a prediction error (RMSE) of ~$42,000.
Outperformed linear regression and demonstrated robustness.
Results
Clustering:
Inland homes and coastal homes formed distinct groups.
Prediction:
Random forest model effectively predicted housing prices.
Classification:
Inland and near-ocean homes were most accurately classified.
Conclusion
Despite the dataset's age, this project provided valuable insights into housing trends and served as a robust practice in data cleaning, modeling, and visualization. Random forest proved the most effective model for predicting housing prices.
