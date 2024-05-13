# Automated Machine Learning Model Trainer

## Overview
This repository contains a Python function for automating the process of training and testing machine learning models. The function takes input in the form of a JSON file containing details about the dataset, preprocessing steps, and the choice of algorithm for classification or regression tasks. It uses grid search cross-validation to tune hyperparameters and provides evaluation metrics such as classification report for classification problems and RMSE, R^2, and adjusted R^2 for regression problems.

## Usage
1. Create a JSON file specifying the details of your dataset, preprocessing steps, and algorithm choice. See the examples  provided in the repository.

2. Use the `automated_ml_trainer` function to train and test your model.

3. The function will perform grid search cross-validation to tune hyperparameters, train the model, and output evaluation metrics based on the problem type (classification or regression).

## Important Details
- `"problem_type"`: Specifies the type of problem (classification or regression).
- `"algorithm"`: Specifies the choice of algorithm (RandomForestClassifier, DecisionTreeRegressor, etc.).
- `"dataset_path"`: Path to the dataset file.
- `"train_test_split"`: Details of train-test split (test_size, random_state, etc.).
- `"preprocessing"`: Dictionary specifying preprocessing steps:
    - `"missing_values"`: Specifies if missing values should be handled (true/false).
    - `"impute_with"`: Specifies the method to impute missing values ([Average of values, Median of values, Mode of values]).
    - `"rescaling"`: Specifies the method for feature rescaling ([MinMaxScaler, StandardScaler]).
    - `"prediction_type"`: Specifies the type of prediction (Regression, Classification).
- All categorical columns will be encoded with one-hot encoder.


