---
layout: post
toc: true
title: "01. Econometrics"
categories: Econometrics
tags: [LLN, CLT, sample, population]
math: true
author:
  - Marco You
[comment]: <> (mathjax inline > \\(...\\) )
[comment]: <> (mathjax block  > $$...$$   )
[comment]: <> <p align="center"> <img src="/image/file_name.png" alt="file_name" width="460" height="260"> </p>
---

**Econometrics Note Chapter 1.**

Personally, I consider econometrics as an application of statistics in economics rather than a sub-branch of economic science. I am stating this because I thought it was some sort of economics when I first saw the name "econometrics". As stated, in this series of notes, 95% of the contents will be about statistics. The other 5% will be economic interpretation of result that comes from statistical analysis.

The main and the most important statistical method that is used in econometrics is **Regression Analysis**. To what is a regression analysis, we need to know how it was created. The term regression was coined by the british anthropologist Francis Galton, also a cousin of Charles Darwin. When he was analyzing the correlation between the size of seeds of pead and the size of successive generations of peas, he found that there is a **linear** trend in the relation between those two observations. All the sets of (seed size,pea size) were more or less above or below **the average** of seed size and pea size coordinate. He called this phenomenon **Regression toward mean**.

## 1. Linear Fitting Problem

Assume that we have a collection of data expressed in coordinates such as

$$ 
(X_i,Y_i)~~~where~i=1,\cdots,n 
$$

and that we would like to describe the relation between X and Y by mean of a **linear relation** \\(Y = \beta_0 + \beta_1 X \\).

Suppose we got a dataset displayed in a scatterplot like below

<p align="center">
<img src="/image/Scatter.png" alt="Scatter" width="300" height="220">
</p>

The best fitting line to these data is

<p align="center">
<img src="/image/fit.png" alt="fit" width="300" height="220">
</p>

There are other possible fitting lines like below

<p align="center">
<img src="/image/fits.png" alt="fits" width="300" height="220">
</p>

why the blue line is the best line? how can we know(measure) it?

One way to proceed the identification of the best fit is to start measuring the **error** of data compared to the fitting line.

<p align="center">
<img src="/image/error.png" alt="error" width="300" height="220">
</p>

Each data is a dot that has \\((X_i,Y_i)\\) coordinates. They are the true **observations** obtained from the true relation equation \\(Y_i = \beta_0 + \beta_1 X_i\\). The blue fitting line is a linear projection of **estimated values** obtained from the estimated relation equation \\(\hat{Y}_i = \hat{\beta}_0 + \hat{\beta}_1 X_i \\\). The black segments represent the **error** we make by substituting \\(Y_i\\) with \\(\hat{Y}_i\\), that is

$$
Error_i = Y_i - \hat{Y}_i = Y_i - \hat{\beta}_0 - \hat{\beta}_1 X_i
$$

Note that we have errors **because we are trying to find a linear fit** to the dataset. Errors do not exist if we do not try to find a linear fit.

Let's now focus on the error, \\( Y_i - \hat{Y}_i \\).

We need to get an **overall measure** of the all errors for each point.

We could think of summing up all the errors like

$$ \sum(Y_i - \hat{Y}_i) $$

But is this a suitable measure? The answer is no. There are 2 problems.

- Problem 1: A part of errors will be canceled out because some errors are positive and some others are negative;
- Problem 2: We consider that small errors and big errors have the same importance. We might want to penalise big errors.

**Solution to Problem 1 and 2**

To neutralize the effect of possible cancellations of positive and negative errors, we define the **overall error** as the Sum of Squared Residuals written as

$$ SSR = \sum(Y_i - \hat{Y}_i)^2 $$

By squaring the error term, we amplify bigger errors. This approach of assessing the error terms is the core idea in **Ordinary Least Squares** approach of estimating "good" estimates for \\(beta_0\\) and \\(\beta_1\\).

## 2. Ordinary Least Squares (OLS)

We assume thet he **size of the mistake** is measured by SSR denoted as

$$ SSR = \sum^n_{i=1}(Y_i - \hat{Y}_i)^2 = \sum^n_{i=1}\hat{u}^2_i $$