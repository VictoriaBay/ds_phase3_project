# SyriaTel Customer Churn Analysis

![image](https://user-images.githubusercontent.com/117164514/218263478-df38eec8-9987-42a2-8c53-1af0496d85d6.jpg)

## Overview

Across the telecommunication industry, customer churn is one of the most important concerns that directly affect a telecommunication company's business. Hence, companies that are able to successfully predict customer churn will be able to allocate capital and resources more efficiently and thereby improve profitability.

This project analyzes customer churn (customers leaving the provider) data from the telecommunications provider SyriaTel. The main objective of this project is to identify what type of customers were churning and develop a model that could predict whether a customer is likely to churn.

## Business Problem

SyriaTel has been facing a customer churn problem. Based on a data, SyriaTel had a churn rate of ~14%. Churn rate is very important because it is typically more expensive to obtain new customers than to retain existing customer. In order for SyriaTel to improve their churn rate, SyriaTel has me tasked to help them predict which customers are likely to churn and provide actionable recommendations to mitigate churn.

## Data Understanding

I used the SyriaTel Customer Churn dataset. This is a public dataset that contains customer usage patterns and also includes a column delineating whether the customer has churned or not. It is unclear when exactly the data was collected, but it appears to have been made publicly available around 2012. Due to the nature of the 'churn' column, the dataset lends itself towards a binary classification problem, where a machine learning model can be constructed and trained on the data to predict whether a customer will churn or not given their usage patterns. The 'churn' column will be used as our target column in this binary classification problem.

## Exploratory Data Analysis

After some basic data cleaning and reformatting for clarity, I split the dataset into predictors and target for both more streamlined analysis and ultimately to use in the modeling process. EDA found that our target's distribution is fairly imbalanced, with only approximately 14% of the customers in the dataset belonging to the 'churn' class.

<img width="733" alt="image" src="https://user-images.githubusercontent.com/117164514/218263604-57d38668-0f41-4516-b9c2-ba9fb1354d8f.png">

As per this plot we can see that the average monthly phone bill for churned customers is a few dollars higher than it is for customers that with the company. This may imply that these customers are unhappy with the amount they are paying per month, or perhaps think they can find a cheaper rate elsewhere

<img width="765" alt="image" src="https://user-images.githubusercontent.com/117164514/218263670-959b48bc-0f47-4db1-a7c3-d9f773ead2fe.png">

Churned customers were having more customer service calls in the comparison with customers who are with the Syriatel.

<img width="666" alt="image" src="https://user-images.githubusercontent.com/117164514/218263730-bbfbc4cf-c1a9-46a6-b33c-a4807f4fbfe1.png">

## Modeling 
* Model1 - Logistic Regression Classifier

Logistic regression is a classification algorithm, used when the value of the target variable is categorical in nature.
It is most commonly used when the data in question has binary output, so when it belongs to one class or another, or is either a 0 or 1.

<img width="676" alt="image" src="https://user-images.githubusercontent.com/117164514/218264018-af34c53c-e4f3-4c75-be7b-44f2048f24a3.png">

* Model2 - Decision Tree Classifier

Decision Tree is a Supervised learning technique that can be used for both classification and Regression problems, but mostly it is preferred for solving Classification problems. It is a tree-structured classifier, where internal nodes represent the features of a dataset, branches represent the decision rules and each leaf node represents the outcome.

It is called a decision tree because, similar to a tree, it starts with the root node, which expands on further branches and constructs a tree-like structure.

<img width="632" alt="image" src="https://user-images.githubusercontent.com/117164514/218264100-305b4498-5a08-41e5-92e7-5e7c69cffb0a.png">

* Model3 - Random Forest Classifier

A forest is comprised of trees. It is said that the more trees it has, the more robust a forest is. Random forests creates decision trees on randomly selected data samples, gets prediction from each tree and selects the best solution by means of voting. It also provides a pretty good indicator of the feature importance.

In machine learning, hyperparameter optimization or tuning is the problem of choosing a set of optimal hyperparameters for a learning algorithm. A hyperparameter is a parameter whose value is used to control the learning process. By contrast, the values of other parameters (typically node weights) are learned.
It is called a decision tree because, similar to a tree, it starts with the root node, which expands on further branches and constructs a tree-like structure.

<img width="545" alt="image" src="https://user-images.githubusercontent.com/117164514/218264158-893c8435-8908-49fe-afc2-7853d025b239.png">

* Model4 Hyperparameter Tuning of Random Forest Classifier

<img width="743" alt="image" src="https://user-images.githubusercontent.com/117164514/218264440-02842eab-b49c-4a56-ad7f-2fa0405062ff.png">

<img width="1121" alt="image" src="https://user-images.githubusercontent.com/117164514/218265439-1bd5519c-0f7e-4b15-8374-f0b471c08fdf.png">

According to the Random Forest Classifier, here are the 3 mostimportant features for the model:
- Total Charge
- Customer Service Calls 
- International Plan 

## Modeling Summary for Model4

* The accuracy score of 0.979 means that the model correctly predicted the outcome for 97.9% of the observations in the test set.

* The F1 score of 0.92308 is the harmonic mean of precision and recall and is used to balance the precision and recall. The higher the F1 score, the        better the balance between precision and recall. In this case, the F1 score of 0.92308 is a good indication that the model has a good balance between precision and recall.

* The recall score of 0.88112 means that the model correctly predicted 88.112% of the positive outcomes in the test set. This score is important when the positive outcome is of great interest and we want to minimize false negatives.

* The precision score of 0.96923 means that when the model predicts positive, it is correct 96.923% of the time. This score is important when false positives are costly and we want to minimize them.

## Recommendations

SyriaTel should prioritize implementing strategies aimed at reducing customer churn, as a loss of 14.8% of their customer base has already been experienced. To achieve this goal, the following initiatives should be considered:

* Rate Assessment

It is essential to evaluate the current charging rates and identify any potential areas for improvement, as customers seem to be dissatisfied with high charges, resulting in increased likelihood of churn.

* Customer Service Evaluation

To improve customer experience, it is crucial to assess the quality of customer service offered by the company. With over 50% of customers making more than three service calls churning, additional training for customer service staff and the creation of an internal forum to document common customer issues should be considered.

* International Plan Analysis

To stay ahead of the competition, it is crucial to investigate the viability of offering an international plan to improve retention and customer satisfaction. A thorough market analysis should be conducted to assess the competitiveness of pricing against other providers, with relevant improvements made to the international plan based on the results.

* Voicemail Plan Promotion

The low number of customers subscribed to the voicemail plan suggests that some customers may be unaware of the option, and therefore promoting this plan may help to reduce churn.

## Repository Guide

* The data used for the project can be found here 
https://github.com/VictoriaBay/ds_phase3_project/blob/main/syria_tel_data.csv

* The notebook that contains the project can be found here 
https://github.com/VictoriaBay/ds_phase3_project/blob/main/Untitled.ipynb

* The presentation for this project can be found here  
https://docs.google.com/presentation/d/1P1Hxa6_1gr7nk6OOYMXXmtJz6LaVlX32NrUgtGJLr9Y/edit?usp=sharing

* A Data Report for this project can be found here 
