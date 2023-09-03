# Kaggle Playground Competition: Feature Selection and Data Preprocessing

This repository contains code and data for a Kaggle Playground competition focused on feature selection, data preprocessing, and model evaluation. The competition's goal is to submit a dataset that will be used to train a random forest regressor model, which will then make predictions against a hidden test dataset.

## Introduction

The competition involves several key steps, including:

1. **Importing Libraries and Dataset**: We begin by importing necessary libraries, such as `numpy`, `pandas`, `matplotlib`, and `sklearn`. The dataset is loaded from a CSV file, and missing values are checked.

2. **Feature Selection**: We use a RandomForestRegressor to select the top 10 features by importance. We then employ an iterative method to try every possible combination of these features, selecting the best combination based on the Root Mean Square Error (RMSE) metric. The iteration continues until no further improvement can be achieved by adding more variables.

3. **Data Preprocessing**: We remove the variables that were not selected in the feature selection process, ensuring that our dataset only contains the most relevant features. Any discarded variables are set to 0.

4. **Model Training**: We use the selected features to train a RandomForestRegressor model with specific parameters, including the number of estimators, maximum depth, and random state. The model is trained on a portion of the dataset, and predictions are made.

5. **Result Submission**: We save the processed dataset to a CSV file named `submission.csv`.

6. **Feature Importance Visualization**: A bar plot is generated to visualize the importance of the selected features.
