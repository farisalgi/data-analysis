# Data Analysis Project

This repository contains Jupyter Notebooks for performing statistical analysis on economic data using GDP and related indicators. This assignment is done for the Data Analysis course.

## Overview

The content performs the following steps:

1. **Data Loading**  
   - Loads `factbookv2.csv` dataset containing economic indicators such as GDP, Exports, Imports, Industrial production growth rate, Investment, and Unemployment rate.

2. **Data Preprocessing**  
   - Cleans numerical columns by removing symbols (e.g., `$`, `,`) and converts them to float values.  
   - Drops rows with missing values.  
   - Prepares the dataset for regression analysis.

3. **Regression Models**  
   - Builds multiple linear regression models with GDP as the dependent variable.  
   - Independent variables include:
     - Exports  
     - Imports  
     - Industrial production growth rate  
     - Investment  
     - Unemployment rate

4. **Statistical Tests**  
   - Calculates predicted GDP values (`y_hat`) for each model.  
   - Computes explained variance (`Rb`) for each regression model.  
   - Performs **F-tests** to check statistical significance of added variables.  
   - Evaluates if each variable remains significant after adding others.

5. **Custom Functions**  
   - `R_2vars(df, var1, var2)` → Computes regression using two independent variables.  
   - `R_3vars(df, var1, var2, var3)` → Computes regression using three independent variables.

## How it works

1. **Simple Regression Models**

   - Builds GDP regression with each variable separately:

      - Model 1: GDP ~ Exports

      - Model 2: GDP ~ Imports

      - Model 3: GDP ~ Industrial production growth rate

      - Model 4: GDP ~ Investment

      - Model 5: GDP ~ Unemployment rate

   - Prints out predicted GDP values and explained variation (Rb).

2. **Significance Testing (F-test)**

   - For example, Model 2 (GDP ~ Imports) is tested:

      - If F-statistic > F-table → Imports significantly affect GDP.

      - Otherwise → not significant.

3. **Two-variable Models**

   - Combines Imports with another variable (Exports, Industrial, Investment, Unemployment).

   - Calculates improvement in explanatory power.

   - F-test checks if adding a new variable is statistically meaningful.

4. **Three-variable Models**

   - Adds a third variable (e.g., Imports + Exports + Industrial production).

   - Checks again whether the new variable improves the model significantly.

   - Also re-checks if older variables remain significant after adding new ones.
