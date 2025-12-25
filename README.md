# Healthcare_Premium_Prediction - Using Machine Learning

## Project Overview

This project focuses on analyzing and predicting annual health insurance premiums using a large real-world dataset of nearly 50,000 policyholders.
The objective is to understand the key drivers of premium pricing and build accurate, business-ready predictive models using both statistical and machine learning approaches.
The project follows a complete end-to-end data science workflow, including data cleaning, exploratory data analysis (EDA), feature engineering, multicollinearity handling, model training, and error analysis.

<img src="https://github.com/GKPSingh/Healthcare_Premium_Prediction/blob/main/Images/hpp.jpg" height=500px width=700px>

## Objectives

* Perform thorough EDA and data cleaning to ensure data reliability
* Identify key factors influencing insurance premiums
* Build and compare regression models
* Diagnose model weaknesses through detailed error analysis
* Propose data segmentation strategies to improve performance


## Dataset Description

* The dataset contains demographic, socioeconomic, lifestyle, and medical information, including:
* Demographics: Age, Gender, Region, Marital Status, Dependents
* Lifestyle: BMI Category, Smoking Status
* Socioeconomic: Income Level, Income (Lakhs), Employment Status
* Medical: Medical History (single & multiple conditions)
* Insurance: Plan Type (Bronze / Silver / Gold)
* Target Variable: Annual Premium Amount
* After cleaning, ~49,900 high-quality records were retained for modeling.


## Data Cleaning & Preprocessing

* Key preprocessing steps included:
* Handling missing values and duplicates
* Correcting invalid values (e.g., negative dependents, unrealistic ages > 100)
* Outlier treatment for age and income
* Standardizing categorical labels (e.g., smoking status)
* One-hot encoding of categorical variables
* Feature scaling using MinMaxScaler

## Exploratory Data Analysis (EDA)

* Insights uncovered:
* Premiums increase strongly with age, insurance plan, and medical risk
* Income influences plan selection but not premium linearly
* Most customers prefer Bronze plans
* Younger customers (≤ 25) exhibit higher relative prediction errors
* Demographic and regional features have limited impact on premiums

## Modeling Approach

Multiple regression models were evaluated:
* Linear Regression
* Ridge Regression	
* XGBoost Regressor	
XGBoost significantly outperformed linear models
Hyperparameter tuning performed using RandomizedSearchCV

## Feature Importance (XGBoost)

Top predictors identified by the final model:

* Insurance plan type
* Age
* Medical risk score
* BMI category (especially obesity)
* Smoking status
* Demographic and regional variables contributed marginally.

## Error Analysis & Key Findings

* While overall accuracy is strong, ~30% of records showed large percentage errors
* Extreme errors are heavily concentrated among younger policyholders (≤ 25 years)

* Nearly all very large errors (>50%) occur in this age group

📌 Insight: A single global model struggles to capture pricing dynamics for young adults.

##  Segmentation Strategy

To address this limitation, the dataset is segmented into:

  * hpp_young → policyholders aged ≤ 25

  * hpp_adult → policyholders aged > 25

This targeted modeling approach is expected to:

  * Reduce extreme percentage errors

  * Improve predictive accuracy

  * Provide age-specific pricing insights

A separate notebook focuses on the premiums_rest (age > 25) dataset.

## Tech Stack

* Python
* Pandas, NumPy
* Matplotlib, Seaborn
* Scikit-learn
* XGBoost
* Statsmodels

## Conclusion

This project demonstrates how combining robust preprocessing, feature engineering, model comparison, and error analysis leads to reliable, business-ready insurance pricing models.
The findings highlight the importance of data segmentation when a single model fails to generalize across distinct customer groups.
