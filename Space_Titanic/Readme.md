# Space Titanic Survival Prediction

## Overview

Predict which passengers of the Spaceship Titanic were transported to an alternate dimension after colliding with a spacetime anomaly. This project provides a complete machine learning workflow from data preprocessing to model predictions.

## Key Steps

1. **Data Loading & Exploration**
   Load the train and test datasets, inspect missing values, and understand feature types.

2. **Data Cleaning & Feature Engineering**
   Handle missing values, split the `Cabin` column into `Deck`, `Cabin_num`, and `Side`, encode boolean and categorical features, and create indicator columns for missing numeric values.

3. **Model Training**
   Train a `RandomForestModel` using TensorFlow Decision Forests. No hyperparameter tuning was applied in this version; the focus was on feature engineering and preprocessing.

4. **Test Data Preprocessing**
   Apply the same transformations to the test dataset as applied to the training dataset.

5. **Prediction & Submission**
   Predict the `Transported` label for each passenger and create a submission CSV file in the required format.

## Notes

* Boolean features (`CryoSleep`, `VIP`) were converted to integers.
* Missing numeric values were filled with 0 or median (for `Age`), with additional `_missing` indicator columns.
* Categorical features (`HomePlanet`, `Destination`, `Deck`, `Side`) were filled with `"Unknown"`.
* Further experimentation with models and hyperparameters may improve results.

## Submission Format

The submission file should be a CSV with the following format:

```
PassengerId,Transported
0013_01,False
0018_01,False
0019_01,True
0021_01,False
...
```

## Evaluation

The competition uses **classification accuracy** as the metric, i.e., the percentage of correctly predicted labels.

## How to view the notebook 

You can view the notebook where I trained the model in this repository, or click [here](https://www.kaggle.com/code/nicklalou/space-titanic-nikos-laloutsos)
to open it directly on Kaggle.

## Acknowledgments

* Kaggle, for the dataset and competition.
* Space Titanic storyline inspired by the Kaggle competition.


