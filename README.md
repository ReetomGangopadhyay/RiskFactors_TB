# Assessing Risk Factors for Treatment Discontinuation in Tuberculosis Patients in Ukraine

This repository contains the code and analysis from our study on treatment adherence in tuberculosis (TB), specifically focusing on the factors influencing patient dropout from TB treatment in Ukraine from 2018 to 2021. The goal of this project is to identify key socio-economic and clinical risk factors that contribute to treatment discontinuation and to provide insights for public health interventions.

## Project Overview:
The study explores patient dropout from TB treatment using a combination of statistical and machine learning techniques:

- Multiple Logistic Regression (R): Establishes relationships between socio-economic, demographic, and clinical factors and treatment dropout.
- LASSO Regression (R): Used for variable selection, narrowing down the most significant predictors.
- Machine Learning Models (Python): Classification and Regression Trees (CART) and HistGradientBoostedClassifier were employed to predict dropout, using GridSearch cross-validation to optimize the models.

## Tools

- R: Used for data wrangling, cleaning, exploratory data analysis (EDA), and statistical modeling (logistic regression, LASSO).
- Python: Employed for machine learning models (CART, HistGradientBoostedClassifier) and model optimization using GridSearch.

## Getting Started

Ensure you have the following software installed:

- R (with necessary libraries: glmnet, dplyr, ggplot2, etc.)
- Python 3.x (with necessary libraries: scikit-learn, pandas, numpy, etc.)
-      additionally make sure your system has enough RAM to properly run the script.




For study results, please refer to the paper contained within this repository. Additionally, please email me if you would like to use any of this code or data for any other projects at rgangopa@bu.edu.
