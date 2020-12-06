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

### 1.1 Random Variable (RV)

**Definition**

**Random variable** X is a variable whose value is determined by the outcome of a random experiment. This is the most simple and intuitive definition of a random variable. 

In formal mathematical terms, we can also say that a random variable is a function defined on a probability space that maps from the sample space to the real numbers, where

- Probability space \\(\equiv (\Omega, \mathcal{F}, \mathbb{P}) \\) where
  - Sample sapce \\(\equiv \Omega \\) is a non-empty set of all possible outcomes (numbers) or results (not numbers) from a random experiment.
  - \\(\sigma\\)-algebra \\(\equiv \mathcal{F}\\) is a set of all possible subsets of \\(\Omega\\), called events. 
  - Probability measure \\(\equiv \mathbb{P}\\) is a function that maps from \\(\sigma\\)-algebra to a probability \\(p \in \[0,1\]\\).

$$ \begin{align}
\Omega &= \{\omega_1, \omega_2 \} \\
\mathcal{F} &= \{\emptyset, \{\omega_1\}, \{\omega_2\}, \{\omega_1, \omega_2\} \} \\
\mathbb{P}(\emptyset) &= p_0 = 0 \\
\mathbb{P}(\{\omega_1\}) &= p_1 = 0,50 \\
\mathbb{P}(\{\omega_2\}) &= p_2 = 0,50 \\
\mathbb{P}(\{\omega_1, \omega_2\}) &= \mathbb{P}(\Omega) = p_3 = 1,00
\end{align}$$

Therefore, a random variable X needs following elements:

- \\( x_1, x_2, \cdots, x_k \\) (k possible outcomes)
- \\( p_1, p_2, \cdots, p_k \\) (probability of each outcome)
- \\( \{x_1, x_2, \cdots, x_k\} \\) (sample space)

where \\(p_i ≥ 0 \\) and \\( \sum^k_{i=1} p_i = 1 \\).

**Random Variable Types**

Outcomes of a random variable could either be **discrete** or **continuous**. In the first case, we call the RV, a **discrete random variable**. In the second case, we call the RV, a **continuous random variable**.

- Discrete random variable example: Rolling a dice,
- Contimnuous random variable example: We choose 

### 1.2 Probability 