# ML Flight Price Prediction Project 

## Project Overview

This project applies machine learning techniques to predict flight prices. The target variable, flight price, is continuous, making this a regression problem.

## Topic Relevance

Predicting flight prices is valuable for consumers. Insights from this model could help optimize ticket purchasing behaviour.

## Data Selection & Preparation

### Dataset

**Size**: 300,000 rows.

**Scope**: Flights between India's top six metro cities.

**Source**: Kaggle (original data scraped from Easemytrip, covering 11 February – 31 March 2022). Found here: https://www.kaggle.com/datasets/shubhambathwal/flight-price-prediction/data

### Features

**Categorical**: Airline, flight, source city, destination city, departure time, arrival time (morning, early morning, afternoon, evening, night, late night), class.

**Continuous**: Duration, days left, price.

### Data Cleaning & Wrangling

Created euro_price column by converting rupee prices using an exchange rate.

Dropped unnecessary columns: unnamed column, flight code, rupee price.

### Feature Engineering & Selection

**Transforming Categorical Variables**

One-Hot Encoding: Applied to airline, source_city, destination_city, departure_time, arrival_time.

Binary Encoding:

class (business/economy) converted to 0/1.

number of stops (zero, one, two or more) converted to 0/1/2.

### Feature Selection

Low correlation among features.

Sufficient correlation between features and target variable.

No features removed.

## Model Building & Evaluation

Model - R² - MAE - RMSE

**KNN Basic**: R² = 0.76

**KNN Normalized**: R² = 0.97

**KNN Standardized**: R² = 0.96

**Linear Regression**: 

R² = 0.91

MAE = 49.39

RMSE = 74.35

**Linear Regression Normalized**: 

R² = 0.91

MAE = 49.39

RMSE = 74.35

**Decision Tree**: 

R² = 0.93

MAE = 38.08

RMSE = 62.89

**Random Forest**: 

R² = 0.96

MAE = 26.35

RMSE =  47.27

**AdaBoost**

R² = 0.98

MAE = 20.16

RMSE = 35.14

**Gradient Boost**: 

R² = 0.9827

MAE = 12.22

RMSE = 32.62

## Key Findings & Insights

High explanatory/prediction power across all models.

**Best performing models**: AdaBoost and Gradient Boost (R² = 0.98) and Normalized KNN (R² = 0.97).

The class variable (business/economy) had the highest impact on price prediction, reducing the influence of other factors.

## Challenges & Learnings

Understanding the scope, gradual content progress, difficulty in selecting a dataset suitable for all applications.

Time Constraints: Limited time led to missed improvements (e.g., transforming duration to an integer format for better interpretation). Could not refine visualizations due to time limitations.

## Future Work & Improvements

**Limitations**

The class variable significantly influenced price prediction.

**Potential Improvements** 

Exclude class from the model. Analyse economy and business class separately to assess the impact of other factors.

## Conclusion

**Strong predictive capability across models.**

**Best models: AdaBoost and Gradient Boost (R² = 0.98).**

**Class dominance reduces the influence of nuanced factors like stops and time of travel.**
