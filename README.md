# Predicting Penalty Kicks with ML models

## Overview

This project was conducted as a component of my Independent Work Study, where, with the aid of the seminar professor, I used Data Science and Machine Learning models to be able to conduct data analysis and draw conclusions after training different types of models on the data. 


A complete report of this project is provided in the repository. However, a quick summary of the report will be provided below as a guide to my work.

## Repo Structure

The repository consists of the following files:

- **no_power_penalty_kick_new_features.csv:** Contains a CSV file of the data that I used for the project.
- **penalty_kick_ml.pdf:** Contains a PDF of the Jupyter Python script.
- **penalty_kick_ml_slides.pdf:** Contains a PDF of the slides I used when I presented my presentation.
- **penalty_kick_ml_video.mp4:** Contains a video recording of my presentation.
- **penalty_kick_models.ipynb:** Contains the Jupyter notebook for the project.
- **written_final_report.pdf:** Contains the written report for the project.

## Abstract

This paper details the design, implementation, and evaluation of a football (soccer in the U.S) penalty predictor that can be used in a myriad amount of ways. This can include teaching goalkeepers whether a penalty will go in based on the penalty kicker’s foot and direction of the ball they shoot. Another way includes predicting penalty kicks for betting purposes, or simply trying to predict whether a penalty kick will go in live, putting features into a model and then comparing them to the user’s guess. This project uses various machine learning models such as decision trees and random forest, to be able to offer the user a simpler way of being able to predict whether a penalty kick will go in or not. This application of a predictor can be used to predict penalty kicks live during nationally televised penalty kick shootout and even be applied for betting purposes of the user.

## Datasets

The dataset that was used for my project was the **no_power_penalty_kick_new_features.csv** dataset, but this dataset was actually formed from a mixture of Kaggle Datasets and my own dataset. 

The datasets are as follows...
 
- **England Premier League Penalty Kicks 2016-2017**: https://www.kaggle.com/code/apopov41/exploring-epl-penalty-kicks-dataset
- **World Cup Penalty Shootouts 1982-2018**: https://www.kaggle.com/datasets/pablollanderos33/ world-cup-penalty-shootouts
- **2019-2020 Penalty Kick Dataset**: https://www.kaggle.com/datasets/emilerichard/ penalty-statistics-20192020
- **Missed Penalty Dataset**: My own recorded dataset of penalties that missed, recorded after watching videos of penalties and recording necessary features in a table.

## Preprocessing & Models

Before integrating my datasets into the model input, I addressed the issue of a limited number of features by consulting with my advisor and deciding to One Hot Encode the categorical data, thereby expanding the features from L’s, R’s, and C’s to 1’s and 0’s, resulting in 8 features. After performing Exploratory Data Analysis, I observed an imbalance in the dataset due to the inherent nature of penalty kick success rates. To address this, I conducted Random Oversampling on the training data, achieving a balanced dataset with 199 penalties going in and 199 penalties not going in. With the balanced training data, the focus shifted to model selection. With this complete, now I was ready to implement my data on machine learning models


After studying the types of machine, I chose a diverse range of machine learning models employed, including Decision Tree, Logistic Regression, Support Vector Machine, Random Forest, and Gradient Boosting. The selection is based on their common usage in machine learning research and their simplicity for efficient training. The models undergo training on oversampled data, followed by hyperparameter tuning using the validation set and evaluation metrics such as F1 and ROC scores to assess their performance in predicting penalty kicks.

## Results

I took the following metrics to determine the best machine learning model. They were
- **ROC Score/ROC curve**
- **F1 Score**
- **Confusion Matrix**

I ended up noticing that the Decision Tree, Gradient Boosting, and Random Forest gave the best metrics because they had the most True False and True Positive occurrences of penalty kicks. The Support Vector Machine, for example, had a very low True Positive value and a rather high True Negative value, whereas the ROC curve for Logistic Regression was barely better than randomly guessing. The graphs and explanation can be referred to in the **penalty_kick_ml_video.mp4** video file as well as the **penalty_kick_ml_slides.pdf** PDF file.

## Room For Improvement

There are 2 ways in which this project could be improved upon. The first way this could be improved would be by adding more features to my machine learning models, which would mean obtaining a larger dataset, and in this case, more penalty kicks. With more features, the goal would be for the models to more accurately predict true positives and true negatives, and to be able to better learn and form predictions. The addition of features leads to my second way to improve this project, which would be to use computer vision to gain more data to analyze, such as body position and shoulder angles, as this is really important when taking a penalty.






