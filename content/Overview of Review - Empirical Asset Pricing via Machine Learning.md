---
title: "Overview of Review - Empirical Asset Pricing via Machine Learning"
tags:
- engagement-paper
- research-review
- economics
- econ5100
---
# Overview of Review - Empirical Asset Pricing via Machine Learning
Using [Critical reading or How To Make Sense of Publish Research](Critical%20reading%20or%20How%20To%20Make%20Sense%20of%20Publish%20Research.md)

My review: [Review - Empirical Asset Pricing via Machine Learning](Review%20-%20Empirical%20Asset%20Pricing%20via%20Machine%20Learning.md)

[Paper link](https://www.nber.org/system/files/working_papers/w25398/w25398.pdf#page=46&zoom=100,84,573)

## Identifying the Author´s Argument
1. What question is the author asking?
How do capable are different machine learning methods to measuring asset risk premia?
More concretely "predicting returns in the cross section and time series"

3. What answer does the author propose (i.e., what is the principle assertion of the study)?
Large economic gains to investors using machine learning forecasts.

5. In what ways does the study improve upon previous research?
Recently, variations of machine learning methods have been used to study the cross section of stock returns. Harvey and Liu (2016) study the multiple comparisons problem using a bootstrap procedure. Giglio and Xiu (2016) and Kelly et al. (2019) use dimension reduction methods to estimate and test factor pricing models. Moritz and Zimmermann (2016) apply tree-based models to portfolio sorting. Kozak et al. (2019) and Freyberger et al. (2019) use shrinkage and selection methods to, respectively, approximate a stochastic discount factor and a nonlinear function for expected returns.

7. How does this the proposed answer compare with that provided by previous research?

9. What are the major logic or theoretical reasons for the author´s argument?

11. What emperical evidence does the author provide?

13. What assumptions is the author making his or her reasoning?

## Evaluating the Author´s Argument
1. Does the theoretical analysis make sense?
2. Are the data used adequate to the task?
3. Does the empirical methodology adequately?
4. Are the assumptions reasonable?
5. Is the analysis (theoretical and empirical) clearly explained?
6. Do the conclusions follow from the evidence presented?
7. On balance, is the author´s argument convincing to you?

## Review Papers Content
- What is the main research question
- Method and data
	- What data is used
	- how many years
	- how to clean data and collect it
- Dependent variables
- Independent variables
- What is done right or wrong, recommendation for improvement

# Notes From Paper
Machine learning Methods: linear regression, generalized linear models with penalization, dimension reduction via principal components regression (PCR) and partial least squares (PLS), regression trees (including boosted trees and random forests), and neural networks.

## Data
We conduct a large scale empirical analysis, investigating nearly 30,000 individual stocks over 60 years from 1957 to 2016.
Predictor set includes 94 characteristics for each stock, interactions of each characteristic with eight aggregate time series variables, and 74 industry sector dummy variables, totaling more than 900 baseline signals.

The immediate implication is that machine learning aids in solving practical investments problems such as market timing, portfolio choice, and risk management, justifying its role in the business architecture of the fintech industry.

## Controlgroup (?)
Consider as a benchmark a panel regression of individual stock returns onto three lagged stocklevel characteristics: size, book-to-market, and momentum.
Lewellen (2015) demonstrates that this model performs about as well as larger and more complex stock prediction models studied in the literature.
R2 from the benchmark model is 0.16% per month for the panel of individual stock returns.
Also controllgroup:

	Our work extends the empirical literature on stock return prediction, which comes in two basic strands. The first strand models differences in expected returns across stocks as a function of stocklevel characteristics, and is exemplified by Fama and French (2008) and Lewellen (2015). The typical approach in this literature runs cross-sectional regressions of future stock returns on a few lagged stock characteristics. The second strand forecasts the time series of returns and is surveyed by Koijen and Nieuwerburgh (2011) and Rapach and Zhou (2013). This literature typically conducts time series regressions of broad aggregate portfolio returns on a small number of macroeconomic predictor variables.

## Findings
1. Machine learning shows great promise for empirical asset pricing.
   R2 into positive territory at 0.11% per month

2. Vast predictor sets are viable for linear prediction when either penalization or dimension reduction is used.
   R2 into positive territory at 0.11% per month. Principal components regression (PCR) and partial least squares (PLS), which reduce the dimension of the predictor set to a few linear combinations of predictors, further raise the out-of-sample R2 to 0.26% and 0.27%, respectively.

4. Allowing for nonlinearities substantially improves predictions.
   Accived with generalized linear models, regression trees, and neural networks.
   monthly stock-level R2 ’s between 0.33% and 0.40%.

5. Shallow learning outperforms deeper learning.
	neural network performance peaks at three hidden layers then declines as more layers are added. Likewise, the boosted tree and random forest algorithms tend to select trees with few “leaves” (on average less than six leaves) in our analysis.

6. The distance between nonlinear methods and the benchmark widens when predicting portfolio returns.
   By aggregating stock-level forecasts from the benchmark three-characteristic OLS model, we find a monthly S&P 500 predictive R2 of −0.22%. The bottom-up S&P 500 forecast from the generalized linear model, in contrast, delivers an R2 of 0.71%. Trees and neural networks improve upon this further, generating monthly out-of-sample R2 ’s between 1.08% to 1.80% per month.

7. The economic gains from machine learning forecasts are large.
   Our tests show clear statistical rejections of the OLS benchmark and other linear models in favor of nonlinear machine learning tools.

8. The most successful predictors are price trends, liquidity, and volatility

9. Better understanding our machine learning findings through simulation.
When we apply our machine learning repertoire to the simulated datasets, we find that linear and generalized linear methods dominate in the linear and uninteracted setting, yet tree-based methods and neural networks significantly outperform in the nonlinear and interactive setting.

## Method:
They compare thirteen models in total, including OLS with all covariates, OLS-3 (which pre-selects size, book-to-market, and momentum as the only covariates), PLS, PCR, elastic net (ENet), generalized linear model with group lasso (GLM), random forest (RF), gradient boosted regression trees (GBRT), and neural network architectures with one to five layers (NN1,…,NN5). For OLS, ENet, GLM, and GBRT, we present their robust versions using Huber loss, which perform better than the version without.

![](attachments/Pasted%20image%2020220929174854.png)
![](attachments/Pasted%20image%2020220929175330.png)
The comparative performance across different methods is similar to the monthly results shown in Table 1, but the annual R2 oos is nearly an order of magnitude larger. Their success in forecasting annual returns likewise illustrates that
machine learning models are able to isolate risk premia that persist over business cycle frequencies and are not merely capturing short-lived inefficiencies.

Figures 4 and 5 demonstrate that models are generally in close agreement regarding the most influential stock-level predictors, which can be grouped into four categories.

The first are based on recent price trends, including five of the top seven variables in Figure 5: short-term reversal (mom1m), stock momentum (mom12m), momentum change (chmom), industry momentum (indmom), recent maximum return (maxret), and long-term reversal (mom36m).

Next are liquidity variables, including turnover and turnover volatility (turn, std turn), log market equity (mvel1), dollar volume (dolvol), Amihud illiquidity (ill), number of zero trading days (zerotrade), and bidask spread (baspread).

Risk measures constitute the third influential group, including total and idiosyncratic return volatility (retvol, idiovol), market beta (beta), and beta-squared (betasq).

The last group includes valuation ratios and fundamental signals, such as earnings-to-price (ep), sales-toprice (sp), asset growth (agr), and number of recent earnings increases (nincr). Figure 4 shows that characteristic importance magnitudes for penalized linear models and dimension reduction models are highly skewed toward momentum and reversal. Trees and neural networks are more democratic, drawing predictive information from a broader set of characteristics.

![](attachments/Pasted%20image%2020220929181507.png)
We also construct eight macroeconomic predictors following the variable definitions detailed in Welch and Goyal (2008), including dividend-price ratio (dp), earnings-price ratio (ep), book-tomarket ratio (bm), net equity expansion (ntis), Treasury-bill rate (tbl), term spread (tms), default spread (dfy), and stock variance (svar).3

![](attachments/Pasted%20image%2020220929182206.png)
All models agree that the aggregate book-to-market ratio is a critical predictor, whereas market volatility has little role in any model.

## Machine Poritfolio
The best 10–1 strategy comes from NN4, which returns on average 2.3% per month (27.1% on an annualized basis). Its monthly volatility is 5.8% (20.1% annualized), amounting to an annualized out-of-sample Sharpe ratio of 1.35

### Simple Linear
The baseline estimation of the simple linear model uses a standard least squares, or “l2”, objective function
$$L(\theta) = \frac{1}{NT}\sum^{N}_{i=1}\sum^{T}_{t=1}(r_{i,t+1}-g(z_{i,t};\theta))^2$$
#### Extension - Robust Objective Function
Can somtimes improve predictive performance by replacing equation (4) with a weighted least squares objective such as
$$L(\theta) = \frac{1}{NT}\sum^{N}_{i=1}\sum^{T}_{t=1}w_{i,t}(r_{i,t+1}-g(z_{i,t};\theta))^2$$

In the machine learning literature, a common choice for counteracting the deleterious effect of heavy-tailed observations is the Huber robust objective function, defined as

$$L(\theta) = \frac{1}{NT}\sum^{N}_{i=1}\sum^{T}_{t=1}H(r_{i,t+1}-g(z_{i,t};\theta), \xi)$$
where
$$
H(x;\xi) =
\Big\{
\begin{matrix}
	x^{2}, \text{ if } |x|\leq \xi;\\
	2\xi |x|-\xi^2, text{ if } |x|\geq \xi.\\
\end{matrix}
$$
The Huber loss, H(·), is a hybrid of squared loss for relatively small errors and absolute loss for relatively large errors, where the combination is controlled by a tuning parameter, ξ, that can be optimized adaptively from the data.
In the empirical analysis they study the predictive benefits of robust loss functions in multiple machine learning methods.

### Penalized Linear
When the number of predictors P approaches the number of observations T, the linear model becomes inefficient or even inconsistent.

Penalized methods differ by appending a penalty to the original loss function
$$L(θ; ·) =L(θ) + φ(θ; ·)$$
There are several choices for the penalty function φ(θ; ·). We focus on the popular “elastic net” penalty, which takes the form
$$\Phi(\theta; \lambda; p) = \lambda(1-p)\sum^{P}_{j=1}|\theta_j|+\frac{1}{2}\lambda p \sum^{P}_{j=1}\theta^2_{j}$$
They adaptively optimize the tuning parameters, λ and ρ, using the validation sample. Our implementation of penalized regression uses the accelerated proximal gradient algorithm and accommodates both least squares and Huber objective functions.

### Dimension Reduction: PCR and PL
…
### Generalized Linear
They first and most straightforward nonparametric approach that they consider is the generalized linear model. It introduces nonlinear transformations of the original predictors as new additive terms in an otherwise linear model. Generalized linear models are thus the closest nonlinear counterparts to the linear approaches.

Forecasting with the generalized linear model can be approached with the same estimation tools as in "Simple Linear". In particular, our analysis uses a least squares objective function, both with and without the Huber robustness modification. Because series expansion quickly multiplies the number of model parameters, we use penalization to control degrees of freedom.

### Boosted Regression Trees and Random Forest
Unlike linear models, trees are fully nonparametric and possess a logic that departs markedly from traditional regressions.
![](attachments/Pasted%20image%2020220929171900.png)

Used boosting and random forest.

### Neural Networks
They are the currently preferred approach for complex machine learning problems such as computer vision, natural language processing, and automated game-playing.
- traditional “feed-forward” networks.
![](attachments/Pasted%20image%2020220929173026.png)
There are many potential choices for the nonlinear activation function (such as sigmoid, hyperbolic, softmax, etc.). We use the same activation function at all nodes, and choose a popular functional form in recent literature known as the rectified linear unit (ReLU), defined as

$$ReLU(x) =
\Big\{
\begin{matrix}
	0, \text{ if } |x|\leq 0\\
	x, \text{ otherwise}\\
\end{matrix}$$

which encourages sparsity in the number of active neurons, and allows for faster derivative evaluation.

In addition to l1 penalization of the weight parameters, we simultaneously employ four other regularization techniques in our estimation: learning rate shrinkage, early stopping, batch normalization, and ensembles
## Critiques
- Are they qualified?
- is the model overfitted?
![](attachments/Pasted%20image%2020220929172723.png)
- Difficult to trust because it is difficult to understand.
- Different controllgroup