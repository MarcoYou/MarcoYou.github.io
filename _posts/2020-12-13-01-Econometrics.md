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

The rest of the note will talk about how to exploit statistical properties from a **random sample** and assimilating them to true statistical properties of the population. In other words, everything will be about:

- Exploiting sample statistical properties;
- Assimilating sample statistical properties to population statistical properties (if possible);
- Establishing the link between sample and population;
- Providing an explanation to a phenomenon;

### 1.2 Sample Mean

Now we know what is a (random) sample, and we know that we have to get its statistical properties. First statistical property to acquire is the **sample mean**. By its appellation, we know that **it is not the population mean**.

Let Y be a random variable and \\(Y_1, \cdots, Y_n\\) are iid.

The **sample mean**, \\(\bar{Y}\\) of the n observations \\(Y_1, \cdots, Y_n\\) is:

$$ \bar{Y} = \frac{1}{n} \sum^n_{i=1}Y_i

Since \\(Y_i\\) are random variables, \\(\bar{Y}\\) is also a random variable. Therefore, the value of \\(\bar{Y}\\) differs from one randomly drawn sample to the others.

Given that \\(\bar{Y}\\) is a random variable, it then has a probability distribution, called sampling distribution