---
title: "My Asset Pricing via Machine learning"
tags:
- 
---
# My Asset Pricing via Machine Learning

This is heavily influenced by
[Review - Empirical Asset Pricing via Machine Learning](Review%20-%20Empirical%20Asset%20Pricing%20via%20Machine%20Learning.md)
and [Review - Empirical asset pricing via machine learning evidence from the European stock market](Review%20-%20Empirical%20asset%20pricing%20via%20machine%20learning%20evidence%20from%20the%20European%20stock%20market.md)

I want to recreate the method they agree is the best. The latter paper is the newest and builds upon the first one. Therefore I am going to try to recreate/find the method they think is the best.

**The method**
1. _stochastic gradient descent_ (SGD) approach to train the neural networks.
2. _batch normalization_ algorithm introduced by Ioffe and Szegedy ([2015](https://link.springer.com/article/10.1057/s41260-021-00237-x#ref-CR58 "Ioffe, S., and C. Szegedy. 2015. Batch Normalization: Accelerating Deep Network Training by Reducing Internal Covariate Shift. In Proceedings of the 32nd International Conference on Machine Learning, 448–456." ))
3. _learning rate shrinkage_
4. _early stopping_, as neural networks aim to minimize the MSFE in the training sample.
5. _ensemble_ approach proposed by Hansen and Salamon ([1990](https://link.springer.com/article/10.1057/s41260-021-00237-x#ref-CR49 "Hansen, L., and P. Salamon. 1990. Neural Network Ensembles. IEEE Transactions on Pattern Analysis and Machine Intelligence 12 (10): 993–1001.")) and Dietterich ([2000](https://link.springer.com/article/10.1057/s41260-021-00237-x#ref-CR26 "Dietterich, T. 2000. Ensemble Methods in Machine Learning. Lecture Notes in Computer Science: Multiple Classifier Systems, 1–15. Berlin, Germany: Springer.")).
6. _dropout_ method applied by Gu at al.(2020), It randomly sets a fraction rate of input variables to exactly zero at each iteration, and thus is one of the most effective methods in the neural network framework to prevent overfitting.

**Portifolio**

The paper might suggest a better solution than Neural network. learning-to-rank (LTR) classification approach

	A classification-based portfolio formation, utilizing a support vector machine that avoids estimating stock-level expected returns, performs even better than the neural network architecture.

	Finally, we challenge the traditional formation process of expected return-sorted portfolios, which uses some statistical prediction model to estimate expected returns first, and selects stocks with the highest expected return forecasts into decile portfolios second. The underlying assumption is that stocks with high expected returns ex ante will deliver high realized returns ex post. Rather than taking the “detour” to estimate stock-level expected returns, we take an alternative approach here. In particular, we use a support vector machine to directly classify stocks into decile portfolios based on linear combinations of predictor variables.

	Finally, we compare the performance of traditional expected return-based portfolio formation with a classification-based approach. In particular, we contrast neural networks (which outperform all other traditional approaches in our empirical analysis) with support vector machines (SVMs). The idea behind SVMs is to search for hyperplanes that territorially divide a multidimensional vector space (our sample of firm observations, consisting of stock-level predictors and decile portfolio labels) into groups of vectors that belong to the same class. This allows for the classification of stocks into decile portfolios without taking the “detour” to predict stock-level expected returns. We find that the classification-based approach is superior to even the best-performing expected return-based portfolio formation because it avoids some of the noise in stock-level returns. Most importantly, it is able to maintain the broad return signal, which is essential for our trading strategy, i.e., the correct classification into a decile portfolio.