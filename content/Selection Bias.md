---
title: "Selection Bias"
tags:
- randomized-trials
- econ5100
- microeconomics
---
# Selection Bias
This is based on the book mastering metrics 1 chapter and is explained with a health insurance example.

We use the letter $Y$ as shorthand for health, the outcome variable of interest.
$Y_i$ is the health of individual $i$.
The road taken without health insurance leads to $Y_{0i}$  for person $i$.
The road with health insurance leads to $Y_{1i}$  for person $i$.
The causal effect of insurance on health is the difference between them, written $Y_{1i} − Y_{0i}$.

In the example we have Khuzdar who have chosen Health insurance and Maria who has not chosen health insurance

![](attachments/Pasted%20image%2020220904162232.png)

The first comparison, $Y_{1,Khuzdar} − Y_{0,Khuzdar}$, is the causal effect of health insurance on Khuzdar, which is equal to 1. The second, $Y_{0,Khuzdar} − Y_{0,Maria}$, is the difference between the two students’ health status were both to decide against insurance. This term, equal to −2, reflects Khuzdar’s relative frailty (weakness/easly sick). In the context of our effort to uncover causal effects, the lack of comparability captured by the second term is called **selection bias**.

We do the following to find the causal effect and selection bias for the average.
$Y_i = Y_{0i} + \kappa <=>  \kappa = Y_i - Y_{0i}$
![](attachments/Pasted%20image%2020220904163034.png)

This equation reveals that health comparisons between those with and without insurance equal the causal effect of interest ($\kappa$) plus the difference in average $Y_{0i}$ between the insured and the uninsured. As in the parable of Khuzdar and Maria, this second term describes selection bias. Specifically, the difference in average health by insurance status can be written:
![](attachments/Pasted%20image%2020220904163351.png)

To fix the selection bias we strive to make [[ceteris paribus]]. This is done by finding the sources of selection bias, such as education. This bias is eliminated by focusing on samples of people with the same schooling, say, college graduates. 

The selection bias is eliminated in [[randomized trials]].

