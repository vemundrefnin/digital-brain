---
title: "Review - Empirical Asset Pricing via Machine Learning"
tags:
- econ5100 
- machine-learning
- engagement-paper 
---
# Review - Empirical Asset Pricing via Machine Learning
Gu: Finding the best machine learning method for stock return prediction.

I looked into the research paper "Empirical Asset Pricing via Machine Learning". The main question this paper try to answer is how capable different machine learning methods are to measure asset risk premia.

There are many different machine learning methods, but this paper focus on a few which the researchers argue is the most relevant based on other research. They refer to a lot of other research throughout the whole paper where they do not explicitly discuss their reasoning. The researchers compare thirteen models in total, which are OLS with all covariates, OLS-3 with pre-selected size, book-to-market and momentum, PLS, PCR, elastic net, generalized linear model with group lasso, random forest, gradient boosted regression trees, and neural network architectures with one to five layers.

The data set used consist of all firms listed on AMEX, NASDAQ and NYSE with samples from 1957 to 2016 with a total of 30,000 stocks.
All methods use covariate from the same set of features. This set of features consist of 94 stock-level predictive characteristics, 74 industry dummies, and 8 macro predictors. The data from 1957 to 2016 are divided into three groups, 18 years of training sample, 12 years of validation sample, and the remaining 30 years for out-of-sample testing.

To measure the results for the machine learning methods they need to compare the results to something well known. In many out-of-sample forecasting applications, predictions are compared against historical mean returns. This has some flaws that is avoid by benchmarking $R^2$ against a forecast value of zero. $R^2$ is used to evaluate the performance of each method.
$$R^2_{oos}=1-\frac{\sum_{(i,t\in \tau_3)}{(r_{i,t+1}-\hat{r}_{i,t+1})^2}}{\sum_{(i,t\in \tau_3)}r^2_{i,t+1}}$$
where $\tau_3$ indicates the out-of-sample testing data, $r_{i,t+1}$ is an asset’s return in excess of the risk-free rate and d $\hat{r}_{i,t+1}$ denote the fitted model and its ensuing return forecast. This $R^2_{oos}$ is used in a Diebold-Mariano test to determine whether the two forecasts are significantly different.

After performing the comparisons between all the methods they have multiple conclusions, here are the ones I think is the most important
1. "Machine learning shows great promise for empirical asset pricing. R2 into positive territory at 0.11% per month."
2. "Vast predictor sets are viable for linear prediction when either penalization or dimension reduction is used"
3. "Allowing for nonlinearities substantially improves predictions"
4. "Shallow learning outperforms deeper learning"
5. "The distance between nonlinear methods and the benchmark widens when predicting portfolio 5 returns."
6. "The economic gains from machine learning forecasts are large."
7. "The most successful predictors are price trends, liquidity, and volatility."

I think the findings of this paper is very interesting. In my opinion the credibility of this research are weakened by the share complexity of both machine learning and the stock market. The credibility might be improved if I read all the referenced material and appendixes. That might also strengthen the connection between their findings and the results for the methods they are representing, which is not very intuitive to understand just form reading the paper.