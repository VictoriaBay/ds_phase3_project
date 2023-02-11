# SyriaTel Churn Modeling

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


