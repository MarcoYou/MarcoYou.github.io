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

## 1. Portfolio Selection

The title seems it has a relation with Pr Markowitz's Portfolio Selection Theory but well... it does not (slightly yes because he basically founded everything).

4 steps:

- Suppose two financial assets (or let's just call them shares) A and B. They are in the same portfolio and being invested on the same arbitrary period generating stochastic (fancy word for random) returns \\(R_A\\) and \\(R_B\\).

- Suppose we invest a unit of investment \\(I\\) (=1) which has following allocations: 
  \\(x\\), proportion for A, and \\((1-x)\\), proportion for B. Let's call future values of shares A and B as \\(V_A\\) and \\(V_B\\).

- Returns of \\(R_A\\) and \\(R_B\\) are determined by:

  $$\begin{matrix} R_A = V_A - 1 \\ R_B = V_B -1 \end{matrix}$$

  Therfore, the return of entire portolio is:

  $$\begin{matrix} R_P = (xV_P + (1-x)V_B) -1 \\ R_P = xR_A + (1-x)R_B \end{matrix}$$

- Since \\(R_A\\) and \\(R_B\\) are both random variables, they both have fisrt-order moment (mean denoted as \\(\mu_i\\) or \\(E(R_i)\\)) and second-order moment (variance denoted as \\( \sigma^2_i \\) or \\( V(R_i) \\)). In consequence, \\(R_P\\) is also a random variable that has mean, variance, and covariance (denoted as \\( \gamma_{ij} \\)):

  $$ E(R_P) = xE(R_A) + (1-x)E(R_B) $$
  $$ V(R_P) = x^2V(R_A) + (1-x)^2V(R_B) + 2x(1-x)Cov(R_A,R_B) $$

  or

  $$ \mu_P = x\mu_A + (1-x)\mu_B $$
  $$ \sigma^2_P = x^2\sigma^2_A + (1-x)^2\sigma^2_B + 2x(1-x)\gamma_{AB} $$

### 1. General Theory
### 2. Demand for Insurance
### 3. Risk Sharing
### 4. Asymmetric Information
### 5. Modelling Risk Aversion
### 6. Intertemporal Decision Making
### 7. Investment Decisions' Timing
