# Predicting-survivals-with-ML

## Introduction
This is a univeristy-based project on a a variant of the famous titanic competition: [spaceship titanic](https://www.kaggle.com/c/spaceship-titanic). Make reference to the [html file](https://github.com/manuelrech/predicting-survivals-with-ML/blob/main/spaceship_titanic_ML.html) or [Rmd file](https://github.com/manuelrech/predicting-survivals-with-ML/blob/main/spaceship_titanic_ML.Rmd) to see all the project.

## Project overview
We have a dataset with many info about passengers in a spaceship that is about to collide with a 'spacetime anomaly' and only some people survived. The purpose of this project is to predict ex-ante which passengers survived and if there was some correlation or causation in the features.

## Features engineering
The original features were:

![alt text](https://github.com/manuelrech/predicting-survivals-with-ML/blob/main/images/str_train_df.png)

where `transported` was the variable to be predicted.
However we noticed that some columns may hide some information, for instance by looking at the head of train

![alt text](https://github.com/manuelrech/predicting-survivals-with-ML/blob/main/images/head_train_df.png)

we notice that 
- `cabin` may be splitted everytime we encounter a '/' so to create 3 new columns
- `passenger_id` may be splitted into 2 colums on the '_' symbol, creating two new columns 

## Models used
This is a binary classification task and therefore we tried a family of methods regarding this problem. We performed 
- Logistic regression
- Shrinkage methods
  - Ridge
  - Lasso
  - Elastic net
- Tree methods
  - Single tree
  - Random Forest
  - Bagging
  - Boosting
- Support Vector Machines
- Non-linar SVM
- NN

## Results
In this table we notice that the best model turned out to be the **Boosting** with 0.8824744 Area Under Curve. 

![alt text](https://github.com/manuelrech/predicting-survivals-with-ML/blob/main/images/results_analysis.png)

## Comments
This was a fun, without real world application project, that however allowed us to face a variety of different models, see how they work, what are the parameters, for which kind of problems they are useful 

 



