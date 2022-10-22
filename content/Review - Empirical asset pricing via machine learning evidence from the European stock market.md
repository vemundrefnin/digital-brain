---
title: "Review - Empirical asset pricing via machine learning evidence from the European stock market"
tags:
- 
---
Drobetz: Use machine learning methods to predict returns in European stocks.

This paper was published in the "Journal of Asset Management"in 2021 and can be seen as an extension to another paper "[Empirical Asset Pricing via Machine Learning](Review%20-%20Empirical%20Asset%20Pricing%20via%20Machine%20Learning.md)" written by Shihao Gu with others. This paper is written by Wolfgang Drobetz proffesor at Hamburg University and Tizian Otto a Ph.D. Candidate and Research Associate at Hamburg University.

This paper look at different machine learning forecasting methods and evaluate their performance of evaluating the returns of European stocks. These methods are ordinary least squares, penalized least squares, principal component regressions, partial least squares, random forests, gradient boosted regression trees, and neural networks.

The data used comes form Thomson Reuters Datastream which includes market and fundamental data for European firms. Unlike the paper by Shihao Gu this paper only have twenty-two firm characteristics in the machine learning methods. Additionally, forty-four dummies which correspond to the ISO country codes and the first two digits of Standard Industrial Classification codes are used in the methods.

The methods are compared to a well known linear benchmark model. This is called the FM regressions approach and is used in paper by Drobetz "Predictability and the Cross Section of Expected Returns: Evidence from the European Stock Market"(2019). They conclude that their machine learning methods beat this benchmark and neural network architecture performs the best. This is also true when accounting for transaction costs.

This paper is written in a way making it easier to understand than
"[Empirical Asset Pricing via Machine Learning](Review%20-%20Empirical%20Asset%20Pricing%20via%20Machine%20Learning.md)". However, I am missing their machine learning implementations in the appendix or references.

