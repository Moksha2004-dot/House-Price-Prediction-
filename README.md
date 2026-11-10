# House Price Prediction Using Machine Learning

## Project Overview

This project focuses on predicting house prices using machine learning techniques and understanding which property features influence selling prices.

Our team worked with the King County House Sales dataset, which contains 21,613 residential property sales. We used Python to explore and clean the data, select important features, and develop prediction models.

We built a Multiple Linear Regression model and compared its performance with a Random Forest model to understand the difference between prediction accuracy and model interpretability.

## Project Objectives

- Explore and understand the housing dataset.
- Clean the data and identify unusual records.
- Identify important factors influencing house prices.
- Perform feature engineering and feature selection.
- Build a Multiple Linear Regression model.
- Compare the results with a Random Forest model.
- Evaluate model performance using different metrics.
- Understand how machine learning can support real estate pricing decisions.

## Tools Used

- Python
- Jupyter Notebook

## Dataset Description

The project uses the King County House Sales dataset, containing 21,613 residential property sales from May 2014 to May 2015.

The dataset includes information such as:

- House prices
- Number of bedrooms and bathrooms
- Living area and lot size
- Number of floors
- Construction grade and condition
- Waterfront access
- Year built and renovation details
- Property location

These variables helped us understand how different property characteristics relate to selling prices.

## Data Exploration and Cleaning

We started by exploring the dataset to understand its structure and identify possible data quality issues.

The original dataset contained 21,613 records and 21 columns.

During data cleaning, we:

- Checked for missing values and duplicate records.
- Identified unusual property information.
- Removed 17 unrealistic records.
- Examined the distribution of house prices.
- Identified high-value properties using the IQR method.
- Retained valid high-price properties to avoid losing useful information.

After cleaning, the dataset contained 21,596 records.

### House Price Distribution

![Distribution of House Prices](./Screenshots/01_data_exploration.png..png)

## Feature Engineering and Selection

We created additional variables to improve the analysis.

These included:

- Sale year
- Sale month
- House age
- Renovation status

We also used correlation analysis to identify important predictors and removed overlapping variables to reduce multicollinearity.

The final model used 15 predictors.

### Correlation Analysis

![Correlation Heatmap](./Screenshots/02_correlation_heatmap.png..png)

## Machine Learning Models

### 1. Multiple Linear Regression

We developed a Multiple Linear Regression model to estimate house prices using property characteristics.

This model was selected because its results are easier to interpret and explain.

It helped us understand how factors such as living area, construction grade, location, and waterfront access are associated with selling prices.

### 2. Random Forest Regression

We also developed a Random Forest model to compare its performance with Multiple Linear Regression.

Random Forest can capture more complex relationships between property features.

The comparison helped us understand the trade-off between prediction accuracy and model interpretability.

## Model Training and Evaluation

We divided the cleaned dataset into:

- 60% training data
- 40% validation data

We evaluated the models using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R-squared (R²)
- Mean Absolute Percentage Error (MAPE)

### Model Performance

| Metric | Multiple Linear Regression |
|---|---|
| Training R² | 0.691 |
| Validation R² | 0.702 |
| Training MAE | $126,499 |
| Validation MAE | $125,357 |
| Validation RMSE | $200,872 |
| Validation MAPE | 25.40% |

### Model Comparison

| Model | Validation MAE |
|---|---|
| Multiple Linear Regression | $125,357 |
| Random Forest | $69,719 |

Random Forest achieved a lower prediction error, while Multiple Linear Regression provided results that were easier to interpret.

## Key Findings

### 1. Living Area Influences House Prices

Living area was one of the strongest predictors of selling price.

The regression model estimated that an additional 100 square feet of living space was associated with approximately $18,200 in higher selling price, holding other factors constant.

### 2. Construction Grade Matters

Homes with higher construction grades generally had higher selling prices.

### 3. Location Plays an Important Role

Geographical location was an important factor in explaining differences in property values.

### 4. Waterfront Properties Have Higher Values

Waterfront access was associated with a substantial increase in predicted house prices.

### 5. Random Forest Improved Prediction Accuracy

Random Forest produced a lower validation MAE than Multiple Linear Regression, suggesting that more complex relationships between property characteristics can improve predictions.

## What I Learned

This project helped me understand how machine learning can be used to solve real business problems.

I gained practical experience in:

- Exploring and cleaning datasets using Python.
- Creating and selecting features.
- Building regression models.
- Evaluating model performance.
- Comparing different machine learning approaches.
- Interpreting results to support business decisions.

The project also helped me understand the importance of balancing prediction accuracy with model interpretability.

## Author

Moksha Ramchetty
