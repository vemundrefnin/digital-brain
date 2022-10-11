---
title: "T-test"
tags:
- #visual-analytics 
- #cis5250
description: "This note was created in the class visual analytics. Additional information was gathererd form investopedia"
---
# T-test
The t-test is a test used for hypothesis testing in statistics and uses the t-statistic, the [t-distribution](https://www.investopedia.com/terms/t/tdistribution.asp) values, and the degrees of freedom to determine statistical significance.

## Which T-test to Use?
![](attachments/Pasted%20image%2020220921184952.png)
Source: https://www.investopedia.com/terms/t/t-test.asp

## Paired Sample T-test
The correlated t-test, or paired t-test, is a dependent type of test and is performed when the samples consist of [matched pairs](https://www.investopedia.com/terms/p/pairstrade.asp) of similar units, or when there are cases of repeated measures. For example, there may be instances where the same patients are repeatedly tested before and after receiving a particular treatment. Each patient is being used as a control sample against themselves.

$$T = \dfrac{mean1-mean2}{\dfrac{s(diff)}{\sqrt{(n)}}}$$
where
$mean1$ and $mean2 =$ the average average value of each sample set
$s(diff)=$ The standard deviation of the differences of the pair values
$n =$ The sample size (the number of paired differences)
$n-1=$ Degrees of freedom

## Equal Variance or Pooled T-Test
The equal variance t-test is an independent t-test and is used when the number of samples in each group is the same, or the variance of the two data sets is similar.

$$T = \dfrac{mean1-mean2}{\dfrac{(n1-1)*var1^2+(n2-1)*var2^2}{n1+n2-2}*\sqrt{\dfrac{1}{n1}+\dfrac{1}{n2}}}$$
Degrees of Freedom $=n1+n2−2$

## Unequal Variance T-Test
The unequal [variance t-test](https://www.investopedia.com/ask/answers/073115/what-assumptions-are-made-when-conducting-ttest.asp) is an independent t-test and is used when the number of samples in each group is different, and the variance of the two data sets is also different. This test is also called Welch's t-test.

$$ T = \dfrac{mean1-mean2}{\sqrt{\dfrac{var1}{n1}+\dfrac{var2}{n2}}}$$

![](attachments/Pasted%20image%2020220921185611.png)
## Class Example
A coffee shop believe average amount of espresso is 4oz.
A random sample of 25 shows a mean of 4.6oz of espresso, and std deviation of .22oz. $\alpha=0.05$

$H_0$: Mean amount of espresso in Q latte is 4oz. $\mu = 4oz$
$H_1$: Mean amount of espresso in Q latte is not 4oz. $\mu \neq 4oz$

$$T = \dfrac{\text{sample mean}-\text{population mean}}{\dfrac{std. deviation}{\sqrt{n}}}$$
$$= \dfrac{4.6-4}{\dfrac{0.22}{\sqrt{25}}} = 13.6$$
[t-table](https://www.sjsu.edu/faculty/gerstman/StatPrimer/t-table.pdf)
Degrees of freedom is $n-1 = 24$
The value form the t-table "critical value" is 2.064
Reject $H_0$ when t-test $>$ critical value.

$13.6 > 2.064$

There is significant difference in the amount of espresso from 4oz

## Class Task
MPG scores:
30, 28, 32, 26, 33, 25, 28, 30
Do the actual MPG deviate significantly form 31 ($\alpha=0.05$)

$H_0: \mu = 31$
$H_0: \mu \neq 31$

Using t-formula we get
$t-value = -2.04$

Using the t-table with degrees of freedom $= 7$ we get
critical value $= 2.365$

Fail to Reject $H_0$ because t-test $<$ critical value.
Average MPG did not differ significantly form 31.

# Class Labs
[Submission T-Test 1](Submission%20T-Test%201.md)
[Submission T-Test 2](Submission%20T-Test%202.md)