---
title: Review - Regression Analysis Using Machine Learning Approaches for Predicting Container Shipping Rates
publish: true
tags: 
- research-review
---

Khan: Finding the best machine learning method to predicting shipping container freight rates.

This paper was written by Ibraheem Abdulhafiz Khan a research student in the field of Artificial Intelligence and his colleague Farookh Khadeer Hussain. They investigate the performance of different machine learning methods when predicting the container freight rate in North America.

They get their data from the North American TransBorder Freight dataset from 2006 to 2021 (15 years). 15 features are used and almost 5 million shipping transactions. The amount of shipping transactions do not make sense when looking at the other numbers provided in "Data Collection and Analysis" section and the referred figures. The data is shuffled and split 7:3, with 7 parts training data and 3 parts testing data.

They look at three different machine learning methods. Two ensemble methods which are Random Forest (RF), and Extreme Gradient Boosting (XGBoost) and one artificial neural network method, namely Multi-Layer Perceptions (MLP). The methods es are compared to each other based on mean squared error (MSE), mean absolute error (MAE), root mean squared error (RMSE) and $R^2$.

The results are shown in the following table.
![](attachments/Pasted%20image%2020221021231308.png)
MLP is the most accurate with $R^2=$ `Acceracy` $= 0.98$. It is specified that XGBoost and RF consume fewer resources than MLP and are 3 times faster in terms of training duration.

This paper would be more informative if it had more detailed explanation of their data, data splitting and method comparison. I think the economic value of this paper's conclusions would be greatly improved if they also compared their machine learning methods to simpler statistical methods, for example ordinary least squares (OLS).

