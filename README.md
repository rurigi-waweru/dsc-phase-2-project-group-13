# Kings County Housing Project

## Overview
This project applies the CRISP-DM (Cross Industry Standard Process for Data Mining) methodology.
This project aims to analyze house sales data in King County using regression modeling to estimate house prices and provide insights on how different features, including renovations might impact house prices.

## Table of Contents
- [Kings County Housing Project](#kings-county-housing-project)
  - [Overview](#overview)
  - [Table of Contents](#table-of-contents)
  - [Business Understanding](#business-understanding)
    - [1.1. Project Overview](#11-project-overview)
    - [1.2. Stakeholders:](#12-stakeholders)
    - [1.3. Business Problem:](#13-business-problem)
  - [Data Understanding](#data-understanding)
  - [Data Preparation](#data-preparation)
  - [Modeling](#modeling)
  - [Model Evaluation](#model-evaluation)
    - [Data Split](#data-split)
    - [Performance Metrics](#performance-metrics)
    - [OLS Regression Results](#ols-regression-results)
      - [Key Coefficients](#key-coefficients)
  - [Business Recommendations](#business-recommendations)
    - [1. Feature Impact Analysis](#1-feature-impact-analysis)
    - [2. Renovation and Condition](#2-renovation-and-condition)
    - [3. Handling Multicollinearity](#3-handling-multicollinearity)
    - [4. Further Analysis](#4-further-analysis)
    - [5. Model Improvement](#5-model-improvement)
  - [Deployment](#deployment)
  - [Installation](#installation)
- [Clone the repository](#clone-the-repository)
- [Navigate into the project directory](#navigate-into-the-project-directory)
- [Install dependencies](#install-dependencies)

## Business Understanding
### 1.1. Project Overview
This project aims to analyze house sales data in King County using regression modeling to estimate house prices and provide insights on how different features, including renovations might impact house prices.
### 1.2. Stakeholders:
1. Real Estate Agents; They will us the model to provide advice to homeowners on property values.
2. Homeowners; They will use the model to make informed decisions about buying,selling or renovating homes.
3. Real Estate Agencies; Interested in increasing sales and client satisfaction by providing accurate home value estimates.

### 1.3. Business Problem:
Real Estate agencies need a model to estimate house prices and provide advice to homeowners about how  renovations might increase the estimated values of their homes potentially increasing sales and customer satisfaction.

## Data Understanding
This phase involves exploring and understanding the Kings County housing dataset:
- **Data Sources**: Kings County housing dataset.
- **Features**: Includes variables such as `price`, `bedrooms`, `bathrooms`, `sqft_living`, and `location`.
- **Data Quality**: Assess completeness and accuracy of data. Identify any anomalies or inconsistencies.
- **Target Variable**: `price` – the housing price to be predicted.
- **Predictors**: Features such as `bedrooms`, `bathrooms`, `sqft_living`, etc.

## Data Preparation
Data preparation involves cleaning and transforming the dataset for modeling:
- **Missing Values**: Handle missing values in features.
- **Data Types**: Convert data types as needed (e.g., encoding categorical variables).
- **Multicollinearity**: Check for and address correlated predictors.
- **Normalization**: Normalize numerical features for better model performance.
- **Encoding**: Convert categorical variables into numeric format using one-hot encoding if necessary.

## Modeling
In this stage, we build and refine models to predict housing prices:
- **Model Selection**: Evaluate different regression models such as Linear Regression, Decision Trees, and Random Forests.
- **Overfitting and Regularization**: Implement techniques to avoid overfitting and improve model generalization.
- **Validation**: Use cross-validation to assess model performance on unseen data.
- **Loss Functions**: Employ appropriate loss functions like Mean Squared Error (MSE) for regression tasks.
- **Performance Metrics**: Measure model performance using metrics such as R-squared and Root Mean Squared Error (RMSE).

## Model Evaluation

### Data Split
- **Train-Test Split**: 75.0% - 25.0%

### Performance Metrics
- **Training Score**: 68.07%
- **Test Score**: 64.84%

### OLS Regression Results
- **R-squared**: 0.681
- **Adjusted R-squared**: 0.680
- **F-statistic**: 1567.0
- **Prob (F-statistic)**: 0.00
- **Log-Likelihood**: -2.2124e+05
- **AIC**: 4.425e+05
- **BIC**: 4.427e+05

#### Key Coefficients
- **Waterfront**: +739,900 (Significant)
- **Year Built**: -104,400 (Significant)
- **Grade 13**: +2,219,000 (Significant)

## Business Recommendations

### 1. Feature Impact Analysis
- **Waterfront**: Emphasize waterfront views in marketing materials to highlight the significant price increase associated with this feature.
- **Grade**: Invest in property upgrades to improve the overall grade and thereby increase the property's value.
- **Year Built**: Consider renovating older properties to enhance their value, as newer houses generally command higher prices.

### 2. Renovation and Condition
- **Condition**: Maintain and improve property conditions to maximize value. Properties in better condition achieve higher prices.
- **Bedrooms and Bathrooms**: Evaluate the impact of adding or improving these features, considering their mixed influence on pricing.

### 3. Handling Multicollinearity
- **Multicollinearity**: Address potential multicollinearity issues by removing or combining highly correlated features. Explore Ridge or Lasso regression for better model stability.

### 4. Further Analysis
- **Residual Analysis**: Revisit data transformation methods to address non-normality in residuals and ensure compliance with regression assumptions.
- **Feature Engineering**: Create interaction terms or polynomial features to capture complex relationships and improve model performance.

### 5. Model Improvement
- **Alternative Models**: Experiment with Ridge or Lasso regression to see if they offer better results and manage multicollinearity effectively.
- **Cross-Validation**: Use cross-validation to validate model performance and ensure generalizability.

## Deployment
If the model performs well, it will be deployed for practical use:
- **Automation**: Set up automated pipelines for data processing and predictions.
- **Integration**: Collaborate with stakeholders to integrate the model into existing systems or platforms.
- **Monitoring**: Establish monitoring procedures to track model performance and make updates as needed.

## Installation
Instructions for setting up the project environment.

```bash
# Clone the repository
git clone https://github.com/FS-Moringa/dsc-phase-2-project.git

# Navigate into the project directory
cd dsc-phase-2-project-group-13

# Install dependencies
pip install -r requirements.txt
