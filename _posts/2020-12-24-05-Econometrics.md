---
layout: post
toc: true
title: "05. Econometrics"
categories: Econometrics
tags: [OLS, Estimation, Non-Linear Regression]
math: true
author:
  - Marco You
[comment]: <> (mathjax inline > \\(...\\) )
[comment]: <> (mathjax block  > $$...$$   )
[comment]: <> <p align="center"> <img src="/image/file_name.png" alt="file_name" width="460" height="260"> </p>
---

# Non-Linear Regression Functions

## 1. Introduction

Two types of non-linearity in regression functions:

- Non-linear functions of a single independent varialbe (most prevailing type)
  - Polynomials
  - Logarithms
  - Interactions
  - (these 3 types are all eligible for OLS estimation)
- Regression functions that are non-linear in the parameters (only a sketch here)

We are going to study 2 groups of methods useful when

- the relation between \\(X_1\\) and \\(Y\\) depends on the value of \\(X_1\\) itself;
- the relation between \\(X_1\\) and \\(Y\\) depends on the value of \\(X_2\\)

**examples)**

<p align="center"> <img src="/image/dep-indep.png" alt="dep-indep" width="600" height="400"> </p>

### 1.1 General Approach

In general, the population regression function reads

$$ Y_i = f(X_{1i}, \cdots, X_{ni}) + u_i~~~~~i=1,\cdots,n $$

where f can be a linear or non-linear function.

In the population, the effect on Y of a change in \\(X_1\\), \\(\Delta X_1\\) is:

- \\(\beta_1 \Delta X_1 ~\\) if f is linear;
- \\( f(X_{1i}+\Delta X_{1i}, X_{2i}, \cdots, X_{ni} ) - f(X_{1i}, X_{2i}, \cdots, X_{ni})~  \\) **if f is non linear**

Since this is a population regression function, of course, both \\(\beta_1\\) and \\(f\\) are unknown and need to be estimated by \\(\hat{\beta}_1\\) and \\(\hat{f}\\).

### 1.2 Modeling Non-Linearities

1. Identify a possible non-linear relation based on the underlying economic theory;
2. Specify a non-linear function and estimate its parameters by OLS method;
3. Determine if the non-linear model improves upon a linear model;
4. Plot the estimated non-linear regression function (if possible);
5. Estimate the effect on Y of a change in X.

### 1.3 Notation

How to estimate the effect on Y of a change in X? by measuring the **elasticity**.

The **elasticity** of Y with respect to X is

$$ E \equiv \frac{\frac{\Delta Y}{Y}}{\frac{\Delta X}{X}} = \frac{X}{Y}\frac{\Delta Y}{\Delta X} $$

E gives us the percentage points change of Y associated with a 1% increase in X.

**Note Bene**

Going from 10% to 11% is either a 1 percentage point increase or 10% increase. It is not a 1% increase.

## 2. Polynomial Non-Linear Regression Function

Before getting into it, polynomial specification of non-linear regression function is not frequently used in econometrics modeling.

One way to specify a non-linear regression for \\(X_1\\) is to use a polynomial in \\(X_1\\):

$$ Y = \beta_0 + \beta_{11}X_1 + \beta_{12}X^2_1 + \cdots + \beta_{1r}X^r_1 + u $$

- Obviously this model is easily estimatable with OLS (in R, lm(y ~ X + X^2 + ...))
- With r = 2 and r = 3 we obtain the quadratic and cubic regression models (r = 3 happens almost never)
- Using the F-test and the t-test, you can test hypothesis on the linear vs polynomial nature of the population regression function: \\( H_0:\beta_{12}=0~~vs~~H_1:\beta_{12}≠0\\)
- Interpreting coefficients in a polynomial regression function is not trivial, the best is to plot the function and compute the estimated effect on Y of a change in \\(X_1\\) for different values of \\(X_1\\).

Let's take a simple example.

### 2.1 Quadratic Regression Model

$$ Y_i = \beta_0 + \beta_1 X_{1i} + \beta_2 X^2_{1i} + u_i $$

- \\(\beta_1\\) cannot be anymore the effect on Y of a change of \\(X_1\\) holding \\(X^2_1\\) constant.
- the effect on Y of a change in \\(X_1\\) is indeed given by

$$ \frac{\delta Y}{\delta X_1} = \beta_1 + 2\beta_2 X_1 $$

this depends on the value of \\(X_1\\).

<p align="center"> <img src="/image/polynomial.png" alt="polynomial" width="600" height="400"> </p>

**example)**

We can think of this kind of regression:

$$ Price_i = \beta_0 + \beta_1 Nrooms_i + \beta_2 Nrooms^2_i + u_i $$