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
{ (X_i,Y_i) ; i=1,\cdots,n }
$$

and that we would like to describe the relation between X and Y by mean of a **linear relation** \\(Y = \beta_0 + \beta_1 X \\).