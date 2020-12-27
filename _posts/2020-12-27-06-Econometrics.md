---
layout: post
toc: true
title: "06. Econometrics"
categories: Econometrics
tags: [Panel Data, Fixed Effects]
math: true
author:
  - Marco You
[comment]: <> (mathjax inline > \\(...\\) )
[comment]: <> (mathjax block  > $$...$$   )
[comment]: <> <p align="center"> <img src="/image/file_name.png" alt="file_name" width="420" height="300"> </p>
---

# Regression with Panel Data

## 1. Panel Data

**Panel data** or longitudinal data is a data structure that records data for **n different entities** observed at **T different time periods**. We distinguish between:

- **balanced panel**: each entity coupled with each time period (missing data could exist but every data is coupled between entity and time)
- **unbalanced panel**: at least one entity in one time period missing

Let's take an example of fatalities dataset: collected data on traffic fatalities in the U.S. Entities are the 48 U.S states recorded for 7 years, from 1982 to 1988. It is a balanced panel.

<p align="center"> <img src="/image/panel.png" alt="panel" width="610" height="410"> </p>

## 2. Regression Model with Panel Data

The multi-variable regression model (MRM) in case of a panel data structure with I entities and T time periods in scalar form reads

$$ Y_{it} = \beta_0 + \beta_1 X_{(1,it)} + \beta_2 X_{(2,it)} + \cdots + \beta_k X_{(k,it)} + u_{it} $$

with \\(i = 1, \cdots, I \\) and \\(t = 1, \cdots, T\\).

In matrix form it remains

$$ \mathbf{Y} = \mathbf{X}\beta + \mathbf{u} $$

but now Y and u are two \\( (IT \times 1) \\) sized vectors, X a \\( (IT \times (K+1)) \\) sized matrix and \\(\beta\\) is a \\( ((K+1)\times 1) \\) sized vector.

### 2.1 Regression result: Drink and Drive?

We study how effective various government policies (e.g tax on beer) designed to discourage drunk driving are in reducing traffic deaths.

Since we do not know what to do with observations in different years, we estimate the following regression model of two different time periods

$$ FATAL_{it} = \beta_0 + \beta_1 BEERTAX_{it} + u_{it} $$

where \\(i = 1, \cdots, 48 \\) with \\(t=1982\\) and \\(t=1988\\). Meaning we consider all the 48 states but only the first and the last years. the regression results in R gives us

<p align="center"> <img src="/image/beertax.png" alt="beertax" width="610" height="410"> </p>

As we can see, estimated beertax coefficient in 1982 is statistically insignificant (high p-value) and the one in 1988 is statistically significant (low p-value). How come this happens? **Should we trust these results?**

**The answer is No.**