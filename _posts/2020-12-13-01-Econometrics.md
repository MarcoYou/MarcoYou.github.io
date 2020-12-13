---
layout: post
toc: true
title: "01. Econometrics"
categories: Statistics
tags: [moments, mean, variance, skewness, kurtosis]
math: true
author:
  - Marco You
[comment]: <> (mathjax inline > \\(...\\) )
[comment]: <> (mathjax block  > $$...$$   )
[comment]: <> <p align="center"> <img src="/image/file_name.png" alt="file_name" width="460" height="260"> </p>
---

This course is an introduction to master level Econometrics. It covers linear regression with single and multiple regressors, non-linear effects and models for panel data. It also introduces non parametric techniques applied to density estimation and regression. Applications and examples are developed using R and Python.

## 1. Population and Sample

In any statistical studies, there are population and sample(s). A population is a set that includes individuals that we want to study. A sample is a part of population that includes some individuals that we want to study (e.g every korean male population and some korean male sample).

Almost always, we cannot know all the statistical properties of a population because often it is impossible (how will you assess to every korean male?) or even if it were possible, it is too costly in terms of money and time to do so.

However, it is possible to know **statistical properties of a sample or of multiple samples from a population**. This is the very basic of statistics and econometrics. We are trying to estimate the real statistical porperties of a population through statistical properties of its sample (or samples).

### 1.1 Random Sample

In a **simple random sample**, n objects are drawn randomly from a population where:

- Each object has the same probability of being drawn;
- The value of the random variable Y for the \\(i^{th}\\) randomly drawn oject is denoted \\(Y_i\\);
- Since each object is equally likely to be drawn and the distribution of \\(Y_i\\) is the same for all \\(Y_i\\), random variables \\(Y_1, \cdots, Y_n\\) are said to be **independently and identically distributed (iid)**.

**Nota bene:**
- There is no such thing as pure **random** in real life.
- iid is hardly possible in real life.