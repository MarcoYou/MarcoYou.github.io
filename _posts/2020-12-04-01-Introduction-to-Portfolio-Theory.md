---
layout: post
toc: true
title: "Portfolio Theory Basics"
categories: Portfolio_Theory
tags: [finance, portfolio, CAPM, Markowitz, Black, Scholes, Merton]
math: true
author:
  - Marco You
[comment]: <> (mathjax inline > \\(...\\) )
[comment]: <> (mathjax block  > $$...$$   )
---
This is a note which includes simplified steps before getting to Black-Scholes-Merton Capital Asset Pricing Model (CAPM) and CAPM itself as well. Since I am very lazy, I am skipping important graphical illustration parts and examples. If you find any algebraic error, please do let me know at **gunhoqw20@gmail.com**.

## 1. Portfolio Composition

The title seems it has a relation with Pr Markowitz's Portfolio Selection Theory but well... it does not (slightly yes because he basically founded everything).

4 steps:

- Suppose two financial assets (shares, bonds etc) A and B. They are in the same portfolio and being invested on the same arbitrary period generating stochastic (fancy word for random) returns \\(R_A\\) and \\(R_B\\).

- Suppose we invest a unit of investment \\(I\\) (for instance, 1$) which has following allocations: 
  \\(x\\), proportion for A, and \\((1-x)\\), proportion for B. Let's call future values of shares A and B as \\(V_A\\) and \\(V_B\\).

- Returns of \\(R_A\\) and \\(R_B\\) are determined by:

  $$\begin{matrix} R_A = V_A - 1 \\ R_B = V_B -1 \end{matrix}$$

  Therfore, the return of entire portolio is:

  $$\begin{matrix} R_P = (xV_P + (1-x)V_B) -1 \\ R_P = xR_A + (1-x)R_B \end{matrix}$$

- Since \\(R_A\\) and \\(R_B\\) are both random variables, they both have fisrt-order moment (mean denoted as \\(\mu_i\\) or \\(E(R_i)\\)) and second-order moment (variance denoted as \\( \sigma ^2_i \\) or \\( V(R_i) \\)). In consequence, \\(R_P\\) is also a random variable that has mean, variance, and covariance (denoted as \\( \gamma _{ij} \\)):

### Formula

  $$ E(R_P) = xE(R_A) + (1-x)E(R_B) $$

  $$ V(R_P) = x^2V(R_A) + (1-x)^2V(R_B) + 2x(1-x)Cov(R_A,R_B) $$

  or

  $$ \mu_P = x\mu_A + (1-x)\mu_B $$

  $$ \sigma^2_P = x^2\sigma^2_A + (1-x)^2\sigma^2_B + 2x(1-x)\gamma_{AB} $$

From these formulas, we can have two simple types of portfolio:

- Portfolio containing a risky asset and a non-risky asset;
- Portfolio containing two risky assets

## 2. Portfolio: one risky asset and one non-risky asset

Let A a risky asset and B a non-risky asset attached to a risk-free rate \\( r_f \\). If we apply such composition to previous formula, we get: (Don't forget that we are only investing 1$ still)

$$ \begin{matrix} 
E(R_P) = xE(R_A) + (1-x)r_0 \\
V(R_P) = \sigma^2_P = x^2 \sigma^2_A
\end{matrix} $$