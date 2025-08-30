# 🛒 Walmart Sales Forecasting

## 📋 Overview
This project focuses on forecasting weekly sales for different departments across multiple Walmart stores. Using historical sales data combined with store information and external features, the model predicts future sales patterns to help optimize inventory management and business planning.

## 🔧 Requirements
- Python
- pandas
- numpy
- matplotlib
- seaborn
- xgboost
- scikit-learn
- kagglehub

## 🎯 Objectives
- Analyze historical sales patterns across different stores and departments
- Identify factors affecting sales variations, including seasonality and holidays
- Develop a machine learning model to predict future weekly sales
- Evaluate model performance and visualize predictions against actual sales

## 📊 Datasets
The project utilizes Walmart datasets from Kaggle:
- train.csv: Historical weekly sales data by store and department
- features.csv: Additional data including holidays, temperature, fuel prices, etc.
- stores.csv: Store type and size information

## 🔄 Process

### 1. Data Loading and Preparation
- Imported datasets using kagglehub
- Merged sales data with store information and features
- Cleaned the data by handling missing values and duplicate columns

### 2. Feature Engineering
- Created time-based features (Month, Year, WeekOfYear)
- Generated lag features (previous 1-4 weeks and 52 weeks prior)
- Calculated rolling averages (4-week, 26-week, and 52-week)
- Applied one-hot encoding to categorical variables

### 3. Exploratory Data Analysis
- Analyzed average sales by month, week of year, and year
- Compared sales patterns between holidays and non-holidays
- Examined sales differences across store types
- Visualized rolling averages to understand seasonal patterns

### 4. Model Development
- Split data into training and testing sets (using last 12 weeks as test data)
- Prepared features ensuring consistent columns between training and test sets
- Trained an XGBoost regression model on the prepared data

### 5. Evaluation and Visualization
- Calculated error metrics: RMSE, MAE, and R-squared
- Created time series plots comparing actual vs predicted sales
- Analyzed prediction errors over time to identify patterns

## 📈 Results
The XGBoost model achieved strong performance in predicting Walmart's weekly sales:
- R² score of approximately 0.9829, indicating the model explains about 98% of the variance in weekly sales
- The actual vs predicted sales visualization shows the model accurately captures both the overall trend and seasonal patterns in the data
- The error analysis reveals consistent performance across the prediction timeframe with minimal systematic bias