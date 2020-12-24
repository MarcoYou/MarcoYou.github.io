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