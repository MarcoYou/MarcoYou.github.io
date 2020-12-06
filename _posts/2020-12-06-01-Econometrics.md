---
layout: post
toc: true
title: "01. Econometrics"
categories: Econometrics
tags: [finance, portfolio, CAPM, Markowitz, Black, Scholes, Merton]
math: true
author:
  - Marco You
[comment]: <> (mathjax inline > \\(...\\) )
[comment]: <> (mathjax block  > $$...$$   )
[comment]: <> <p align="center"> <img src="/image/file_name.png" alt="file_name" width="460" height="260"> </p>
---

This is an introduction to master level Econometrics. It covers linear regression with single and multiple regressors, non-linear effects and models for panel data. It also introduces non parametric techniques applied to density estimation and regression. Applications and examples are developed using R and Python.

## 1. Reminder: Statistics 101

### 1.1 Random Variable

**Random variable** X is a variable whose value is determined by the outcome of a random experiment. This is the most simple and intuitive definition of a random variable. 

In mathematical terms (slightly more complex definition), we can also say that a random variable is a function defined on a probability space that maps from the sample space to the real numbers. Therefore, a random variable X needs following elements:

- \\( x_1, x_2, \cdots, x_k \\) (k possible outcomes)
- \\( p_1, p_2, \cdots, p_k \\) (probability of each outcome)
- \\( \{x_1, x_2, \cdots, x_k\} \\) (sample space)

where \\(p_i ≥ 0 \\) and \\( \sum^k_{i=1} p_i = 1 \\).


