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

<p align="center"> <img src="/image/panel.png" alt="panel" width="600" height="410"> </p>

## 2. Regression Model with Panel Data

The multi-variable regression model (MRM) in case of a panel data structure with I entities and T time periods in scalar form reads

$$ Y_{it} = \beta_0 + \beta_1 X_{(1,it)} + \beta_2 X_{(2,it)} + \cdots + \beta_k X_{(k,it)} + u_{it} $$

with \\(i = 1, \cdots, I \\) and \\(t = 1, \cdots, T\\).

In matrix form it remains

$$ Y = X\beta + u \mathcal{u} \mathcal{X} \mathbf{X}$$