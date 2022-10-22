---
title: "Week 5 Methodology Case Study - Differences in Differences"
tags:
- econ5100
---
# Week 5 Methodology Case Study - Differences in Differences
- Causal interference
- Difference in Difference analysis
- Examples:
	- Unilateral Divorce
	- Abortion

## Causality in Econometrics -The Rubin Causal Model
From youtube video of ben lambert.

X -> Y
X "causes" Y

Example:
Infrastructure -> Decrease in Violence
$D_i=0$, No policy, Average level of violence: 100
$D_i=1$, Policy, Average level of violence: 150

This is not what we expected. We wanted Infrastructure to cause Decrease in violence. Instead it looks like decrease in violence cause more infrastructure spending. This is what we call selection bias.

$$
\text{potential violence=}
\begin{bmatrix}
V_{1i} \text{, if } D_{i}=1\\
V_{0i} \text{, if } D_{i}=0
\end{bmatrix}
= \delta=V_{1i}-V_{0i}
$$
In practice we are after
$$E(\delta) = e(V_{1i})-E(V_{0i})$$

We can separately look at each states that got the policy implemented.
$$D_i=1, V_{1i}-V_{0i}, \text{where } V_{0i} \text{ is the observer and } V_{1i} \text{ is the counterfactual}$$
$$D_i=0, V_{1i}-V_{0i}$$
$$E(V_{1i}-V_{0i}) = E(v_{1i}|D_i=1)-E(v_{0i}|D_i=1)$$

## Simple Difference in Difference Analysis
[Another youtube video.](https://www.youtube.com/watch?v=Q5QOCMIwjbg&ab_channel=MikeJonasEconometrics)

Estimate impact of a treatment of a given outcome over time. impact of tutoring on students GPA?

Want to look at the **difference in the changes** over time across groups.
Type B is treated.
Type A is the control group, did not receive treatment.
$\delta_{DD} =\text{Effect of treatment on outcome } Y$
$\delta_{DD} =(\bar{Y}_{B,2}-\bar{Y}_{A,2})-(\bar{Y}_{B,1}-\bar{Y}_{A,1})$
Formula: Differences after treatment minus differences before treatment.

Can also be written:
$\delta_{DD} =(\bar{Y}_{B,2}-\bar{Y}_{B,1})-(\bar{Y}_{A,2}-\bar{Y}_{A,1})$
Formula: How did things change if you where in the group B minus how did things change if you where in the group A

Counterfactual Treatment Group outcome:
What would the treatment group outcome be treatment, if treatment had not occurred? This can not be answered because we do not know, it can not be observed.
It would, by assumption, follow the same trend as the control group.
Counterfactual outcome will be the original mean in period 1($Y_{B,1}$) plus the change experienced by the control group ($\bar{Y}_{A,2}-\bar{Y}_{A,1}$)

|                  | Control (A) | Treated (B) | Counterfactual |
| ---------------- | ----------- | ----------- | -------------- |
| Pre-Treatment(1) |$Y_{A,1}$             |$Y_{B,1}$             |                |
| Post-Treatment(2)|$Y_{A,2}$             |$Y_{B,2}$             |                |
![](attachments/Pasted%20image%2020220927192205.png)

Parallel trends:
We must assume that the trends of dependent variable over time were identical between the treated and non-treated group prior to treatment.
In addition, we assume that the trends would have remained parallel, had it not been for the treatment. Thus any difference in trends can be attributed to the treatment effect.

OLS:
Let $D_{TREATi}=1$ if observation $i$ is in treatment group. $D_{POSTi}=1$ if observation $i$ occurs in post-treatment.
$Y_i=b_0 + \delta_T D_{TREATi} + \delta_P D_{POSTi} + \delta (D_{TREATi})(D_{POSTi})$
OLS estimate of $\delta_{DD}$ will git the ATE (Average Treatment Effect)

## Frekonomics
Abortion:
Legalised abortion 1973 legal nation wide. One of the prime reason crime fell.
Roe v. Wade, data support the hypothesis saying that 18 years later the crime rates should fall.
# General Notes
There is a vote about gambling.
Online betting is going to be used for housing in California.
Policy 27 and 26(?)
It is about more gambling for the tribes and online gambling.

"Trump as president is scary" - Professor

Can not go to texas, florida… 22 states. most red states he can not use state money. The money is part of your 10 year professor plan.

Should you use median or the mean?
you choose the one that represents the population the best. We call this weighting

Regression continuity and … is the same as Diffrence-in-Diffrences observations.

R squared do not mean a lot for an economist
Important:
- coefiiceint
- statistical significance
- …

Idea for paper. Look at some evironmental changes in other markets that is going to happen i the fish market. For esample taxing envriomental fotprint.



