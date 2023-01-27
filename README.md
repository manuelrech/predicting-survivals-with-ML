# Predicting-survivals-with-ML

## Overview
This project is a data science exploration of the Spaceship Titanic dataset, a [variant](https://www.kaggle.com/c/spaceship-titanic). Make reference to the [html file](https://github.com/manuelrech/predicting-survivals-with-ML/blob/main/spaceship_titanic_ML.html) of the famous Titanic competition on Kaggle. The goal of this project is to predict the survival of passengers in a spaceship that is about to collide with a 'spacetime anomaly' using advanced machine learning techniques. The project report can be found in the [html file](https://github.com/manuelrech/predicting-survivals-with-ML/blob/main/spaceship_titanic_ML.html) or the [Rmd file](https://github.com/manuelrech/predicting-survivals-with-ML/blob/main/spaceship_titanic_ML.Rmd).

## Features engineering
The original features were:

![alt text](https://github.com/manuelrech/predicting-survivals-with-ML/blob/main/images/str_train_df.png)

where `transported` was the variable to be predicted.

The original dataset included features such as `cabin` and `passenger_id` that contain hidden information. For example, by splitting the `cabin` column every time we encountered a '/', we were able to create 3 new columns. Similarly, by splitting the passenger_id column on the '_' symbol, we were able to create 2 new columns.

## Models used
This project is a binary classification task, we tried several machine learning models, including
- Logistic regression
- Shrinkage methods (Ridge, Lasso, Elastic net)
- Tree methods (Single tree, Random Forest, Bagging, Boosting)
- Support Vector Machines (Linear and non-linear)
- NN

## Results
Our analysis revealed that the best model was **Boosting** with an impressive Area Under the Curve of 0.8824744.

![alt text](https://github.com/manuelrech/predicting-survivals-with-ML/blob/main/images/results_analysis.png)

## Relevant columns + charts
`Spa`, `VRDeck` and `CryoSleep` turned out to be the most relevant features in terms of Mean Decrease in Gini Index for the tree-based methods. Let's look at the charts we did ex-ante to see if this was visually intuible:

![alt text](https://github.com/manuelrech/predicting-survivals-with-ML/blob/main/images/chart_cryosleep_transported.png)

Cryosleep was super clear, however for numerical columns we struggle to see this evidence because there are some extremeli high values that skew the data to the right

![alt text](https://github.com/manuelrech/predicting-survivals-with-ML/blob/main/images/spa_transported.png)

## Comments
This was an exciting and enlightening project that allowed us to dive deep into the dataset and uncover hidden insights. We were able to experiment with a variety of different models and understand their parameters and appropriate use cases.
 



