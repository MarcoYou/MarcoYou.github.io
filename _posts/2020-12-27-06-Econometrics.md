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

<p align="center"> <img src="/image/panel.png" alt="panel" width="500" height="420"> </p>