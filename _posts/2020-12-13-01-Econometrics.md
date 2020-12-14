---
layout: post
toc: true
title: "01. Econometrics: LLN and CLT"
categories: Econometrics
tags: [LLN, CLT, sample, population]
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