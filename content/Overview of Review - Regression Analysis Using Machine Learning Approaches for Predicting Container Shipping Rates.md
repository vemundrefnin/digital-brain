---
publish: false
title: Words
tags: 
- research-notes
- econ5100
- deep-learning
- random-rorest 
- extreme-gradient-boosting 
- multi-layer-perceptions 
- forecast-models
- container-freight-rate
---

[Paper link](https://link.springer.com/content/pdf/10.1007/978-3-030-99587-4_23.pdf)

[[Review - Regression Analysis Using Machine Learning Approaches for Predicting Container Shipping Rates]]

authors: Ibraheem Abdulhafiz Khan and Farookh Khadeer Hussain

	This research is dedicated to investigating and predicting shipping containerised freight rates using machine learning approaches and real-time data to uncover superior forecasting methods. Ensemble models including Random Forest (RF) and Extreme Gradient Boosting (XGBoost), and deep learning, in particular Multi-Layer Perceptions (MLP) have all been used to provide data-driven predictions after initial feature engineering. These three regression-based machine learning (ML) models are used to predict the container shipping rates in the North American TransBorder Freight dataset from 2006 to 2021. It has been found that MLP surpasses ensemble models with a test accuracy rate of 97%. Although our findings are drawn from American shipping data, the proposed approach serves as a general method for other international markets.

# Words
- ultra-large container ships (ULCS)
- Random Forest (RF)
- machine learning (ML)
- Multi-Layer Perceptions (MLP)
- Extreme Gradient Boosting (XGBoost)
- Artificial Neural Networks (ANNs)
- mean squared error (MSE)
- mean absolute error (MAE)
- root mean squared error (RMSE)

# Comments
I think i like that they are explaining overall level of information

# Critics
Figures are not nice and are lacking text.
Is USA included or is it only Canada and Mexico.
Noticed that this had some small deatials missing. Such as inconsistent number syntax:
100000 != 100,000.
A lot of obvious facts compared to other papers.
Do not explain how they tune their model.
	This can be particularly important when comparing how different Machine Learning models performs on a dataset. In fact, it would be unfair for example to compare an SVM model with the best Hyperparameters against a Random Forest model which has not been optimized.

Feels unprofessional "It is critical to keep track of the model code,…"

the amount of years that is predicted is not specified, but can be calculated because it is 30% of the timeperiod between 2006 to 2021. But this do not seem to be tha case because: "We shuffled the data to induce any imbalance in progressive regression analysis" How did they shuffel the data?
What is the real usecase then?

I feel like their are missing comparisons to very simple statistical methods.

The use of R-squared is not a good indicator of which model is best.
read more about that in this article: [R squared Does Not Measure Predictive Capacity or Statistical Adequacy](https://www.kdnuggets.com/2020/07/r-squared-predictive-capacity-statistical-adequacy.html)
Sometimes The standard error is a better guide.
![](attachments/Pasted%20image%2020221021230046.png)
They have the same $R^2$ with a linear regression model. The standard error would have been a much better guide being roughly seven times smaller in the first case.
