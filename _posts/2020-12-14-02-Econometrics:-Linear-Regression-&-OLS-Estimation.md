---
layout: post
toc: true
title: "02. Econometrics: Linear Regression & OLS Estimation"
categories: Econometrics
tags: [OLS, Estimation, Linear Regression]
math: true
author:
  - Marco You
[comment]: <> (mathjax inline > \\(...\\) )
[comment]: <> (mathjax block  > $$...$$   )
[comment]: <> <p align="center"> <img src="/image/file_name.png" alt="file_name" width="460" height="260"> </p>
---

In this second note for econometrics, I will talk mainly talk about ordinary least squares estimation method using simple linear regression model with one regressor.

## 1. Linear Regression Model with one regressor

From this moment, all random samples imply iid.

In its simplest form, the linear regression model can be expresseda as

$$
Y_i = \beta_0 + \beta_1 X_i + u_i
$$

where \\(\beta_0 + \beta_1 X_i \\) is the **Population Regression Function** attempting to capture the **Conditional Expectation Function**.

As it was mentionned before, we do not have access to the entire population but only to a random sample drawn from the population.

## 2. OLS Estimates

Using a random sample drawn from the population, we can obtain the OLS **estimates** of \\(\beta_0\\) and \\(\beta_1\\) using

$$
\begin{cases}
\hat{\beta}_0 = \overline{Y} - \hat{\beta}_1 \overline{X} \\
\hat{\beta}_1 = \frac{\sum_i(X_i - \overline{X})(Y_i-\overline{Y})}{\sum_i (X_i - \overline{X})^2}
\end{cases}
$$

The above equation system comes from the FOC of the OLS problem which is

$$
\min_{\hat{\beta}_0,\hat{\beta}_1} \left[ \sum_i(Y_i - \hat{Y}_i)^2 = \sum_i(Y_i - \hat{\beta}_0 -\hat{\beta}_1X_i)^2 \right]
$$

This minimisation problem implies **minimisation of the gap between actual \\(Y_i\\) and the estimated \\(\hat{Y}_i\\)**, where \\( \hat{\beta}_0 -\hat{\beta}_1X_i \\) is the **Sample Regression Function**, and \\( \hat{Y}_i = \hat{\beta}_0 + \hat{\beta}_1X_i \\) is the fitted value of \\(Y_i\\) and \\( Y_i - \hat{Y}_i = \hat{u}_i \\), the **residual of the regression**.