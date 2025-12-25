# Healthcare_Premium_Prediction - Using Machine Learning

## Project Overview

This project focuses on analyzing and predicting annual health insurance premiums using a large real-world dataset of nearly 50,000 policyholders.
The objective is to understand the key drivers of premium pricing and build accurate, business-ready predictive models using both statistical and machine learning approaches.
The project follows a complete end-to-end data science workflow, including data cleaning, exploratory data analysis (EDA), feature engineering, multicollinearity handling, model training, and error analysis.

<img src="https://github.com/GKPSingh/Healthcare_Premium_Prediction/blob/main/Images/hpp.jpg" height=700px width=900px>

## Objectives

Perform thorough EDA and data cleaning to ensure data reliability

Identify key factors influencing insurance premiums

Build and compare regression models

Diagnose model weaknesses through detailed error analysis

Propose data segmentation strategies to improve performance


## Dataset Description

The dataset contains demographic, socioeconomic, lifestyle, and medical information, including:

Demographics: Age, Gender, Region, Marital Status, Dependents

Lifestyle: BMI Category, Smoking Status

Socioeconomic: Income Level, Income (Lakhs), Employment Status

Medical: Medical History (single & multiple conditions)

Insurance: Plan Type (Bronze / Silver / Gold)

Target Variable: Annual Premium Amount

After cleaning, ~49,900 high-quality records were retained for modeling.


## Data Cleaning & Preprocessing

Key preprocessing steps included:

Handling missing values and duplicates

Correcting invalid values (e.g., negative dependents, unrealistic ages > 100)

Outlier treatment for age and income

Standardizing categorical labels (e.g., smoking status)

One-hot encoding of categorical variables

Feature scaling using MinMaxScaler
