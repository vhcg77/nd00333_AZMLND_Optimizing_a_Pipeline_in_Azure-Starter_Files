# Optimizing an ML Pipeline in Azure

## Overview
This project is part of the Udacity Azure ML Nanodegree.
In this project, we build and optimize an Azure ML pipeline using the Python SDK and a provided Scikit-learn model.
This model is then compared to an Azure AutoML run.

## Summary
This dataset contains data about employee loans, including variables like job, marital status, education, among others. Therefore, the goal is to predict if it is possible to deliver loans based on the previous variables. A logistic regression algorithm was used for solving this problem. After a successful hyperparameter selection, a selected model was capable of reaching an accuracy of 90.9%.

## Scikit-learn Pipeline

The Scikit-learn Pipeline contains a command to import the data from a CSV file, a function to clean and preprocess the data, and a logistic algorithm. The preprocess functions replace the categories for marital, default, housing, loan, and outcome by 1 or 0. A one-hot encoding is applied to the variables contact and education. 

The hyperparameters solver, C, and max_iter were used to perform this hyperparameter search. Using these hyperparameters was beneficial because there is a broader possibility of hyperparameters selection. Therefore, the higher the probability of reaching the best accuracy.

## AutoML
The AutoML finds among the available Machine Algorithms to find the best that fits the actual problem. Therefore, you only have to select the type of problem (regression or classification), the target variable, cross-validation if needed, and the metric used to maximize. The metric used was accuracy; the target is "y"; cross-validation with 5-fold is used. The training was limited to 30 minutes for each iteration.


## Pipeline comparison
The hyperparameter search and AutoML pipeline took similar execution times. Despite that, AutoML gives an accuracy of 91.74% higher than 91.00%. Therefore, the performance of AutoML is the best between both pipelines.

## Future work

There are many ways in which these steps can be improved. The following steps can be proposed to improve both pipelines:
- Perform an Exploratory Data Analysis to understand better the business logic.
- Develop more feature engineering using the previous business logic.
- Include Deep Learning Algorithms.
- Perform an analysis of the balance of data.
