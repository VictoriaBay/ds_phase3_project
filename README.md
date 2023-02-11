# SyriaTel Churn Modeling

## Overview

Across the telecommunication industry, customer churn is one of the most important concerns that directly affect a telecommunication company's business. Hence, companies that are able to successfully predict customer churn will be able to allocate capital and resources more efficiently and thereby improve profitability.

This project analyzes customer churn (customers leaving the provider) data from the telecommunications provider SyriaTel. The main objective of this project is to identify what type of customers were churning and develop a model that could predict whether a customer is likely to churn.

## Business Problem

SyriaTel has been facing a customer churn problem. Based on a data, SyriaTel had a churn rate of ~14%. Churn rate is very important because it is typically more expensive to obtain new customers than to retain existing customer. In order for SyriaTel to improve their churn rate, SyriaTel has me tasked to help them predict which customers are likely to churn and provide actionable recommendations to mitigate churn.

## Data Understanding

I used the SyriaTel Customer Churn dataset. This is a public dataset that contains customer usage patterns and also includes a column delineating whether the customer has churned or not. It is unclear when exactly the data was collected, but it appears to have been made publicly available around 2012. Due to the nature of the 'churn' column, the dataset lends itself towards a binary classification problem, where a machine learning model can be constructed and trained on the data to predict whether a customer will churn or not given their usage patterns. The 'churn' column will be used as our target column in this binary classification problem.
