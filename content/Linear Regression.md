---
title: "Linear Regression"
tags:
- data-mining 
- cis5550
- machine-learning 
---

$$Y=\beta_0 + \beta_1 X + \epsilon$$
where $\beta_0$ and $\beta_0$ are two unknown constants that represent
the intercept and slope, also known as coefficients or parameters,
and $\epsilon$ represents the error term.

Given some estimates $\hat\beta_0$ and $\hat\beta_1$, for the model coefficients,
we predict future sales using
$$\hat{Y}=\hat\beta_0 + \hat\beta_1 x$$
where $\hat{Y}$ indicates a prediction of $Y$ on the basis of $X = x$.

# Regression as an Explanatory Model
Y (dependent variable ) based on X (independent variable )
- If a person’s age increases, how will the income change?
- If the amount of TV ads increases, how will the company’s sales change?
- If the number of steps per day increases, will does the person’s weight change?
# Regression as a Predictive Model
Predict Y (Dependent variable), based on X(Independent variable)
- Predict a person’s income based on age, gender, education, etc.
- Predict a company’s sales based on the amount of TV ads, radio ads, etc.
- Predict a person’s weight based on the number of steps taken per day

# Ordinary Least Square (OLS)
Used to make the best linear regression line.
![](attachments/Pasted%20image%2020221020200052.png)
$$\hat{\beta_1}=$$
$$\hat{\beta_0}=\bar{y}-\hat{\beta_1}\bar{x}$$

