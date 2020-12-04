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

  $$\begin{align} R_A &= V_A - 1 \\ R_B &= V_B -1 \end{align}$$

  Therfore, the return of entire portolio is:

  $$\begin{align} R_P &= (xV_P + (1-x)V_B) -1 \\ R_P &= xR_A + (1-x)R_B \end{align}$$

- Since \\(R_A\\) and \\(R_B\\) are both random variables, they both have fisrt-order moment (mean denoted as \\(\mu_i\\) or \\(E(R_i)\\)) and second-order moment (variance denoted as \\( \sigma ^2_i \\) or \\( V(R_i) \\)). In consequence, \\(R_P\\) is also a random variable that has mean, variance, and covariance (denoted as \\( \sigma _{ij} \\)). This gives the formulae below:

$$ \begin{align} E(R_P) &= xE(R_A) + (1-x)E(R_B) \\ V(R_P) &= x^2V(R_A) + (1-x)^2V(R_B) + 2x(1-x)Cov(R_A,R_B) \end{align} $$

or

$$\begin{align} \mu_P &= x\mu_A + (1-x)\mu_B \\ \sigma^2_P &= x^2\sigma^2_A + (1-x)^2\sigma^2_B + 2x(1-x)\sigma_{AB} \end{align}$$

From these formulae, we can have two simple types of portfolio:

- Portfolio containing a risky asset and a non-risky asset;
- Portfolio containing two risky assets

## 2. Portfolio: one risky asset and one non-risky asset

Let A a risky asset and B a non-risky asset attached to a risk-free rate \\( r_f \\). If we apply such composition to previous formula, we get: (Don't forget that we are only investing 1$ still)

$$ \begin{align}
E(R_P) &= xE(R_A) + (1-x)r_f \\
V(R_P) &= \sigma^2_P = x^2 \sigma^2_A
\end{align} $$

From \\(V(R_P)\\), we get the following allocation:

$$ x = \frac{\sigma_P}{\sigma_A} $$

from which we can rewrite the expected portfolio return formula as following:

$$ \begin{align} 
E(R_P) &= \frac{\sigma_P}{\sigma_A} E(R_A) + (1-\frac{\sigma_P}{\sigma_A})r_f \\
&= \frac{\sigma_P}{\sigma_A}(E(R_A)-r_f) + r_f
\end{align} $$

Finally with some rearrangement, we get:

$$ E(R_P) = \frac{E(R_A)-r_f}{\sigma_A}\sigma_P + r_f $$

We remark two things from this equation: 
- \\(E(R_P)\\) is a **linear function** of risk (\\(\sigma_P\\)) with risk free rate \\(r_f\\) as y-intercept.
- The slope of this function is called **Sharpe ratio** which is interpreted as **excessive return of share A per each unit of risk undertakend by the share A**.

## 3. Portfolio: two risky assets

Let A and B two different risky assets. We apply the same logic. Then the formula becomes (or stays as):

$$ \begin{align}
E(R_P) &= xE(R_A) + (1-x)E(R_B) \\
V(R_P) &= x^2\sigma^2_A + (1-x)^2\sigma^2_B + 2x(1-x)\sigma_{AB}
\end{align} $$

In this case, the capital allocation line is no longer linear except a particular case when A and B are perfectly and positively correlated. The correlation proxy \\(\rho _{AB}\\) is computed by:

$$ \rho_{AB} = \frac{Cov(R_A,R_B)}{SD(A) \times SD(B)} = \frac{\sigma_{AB}}{\sigma_A \sigma_B} $$

where \\(\sigma _{AB}\\) can be either negative or positive (nul is impossible in real life).

We can find the optimal allocation proportion \\(x\\) by first-order condition of utility function of the portfolio which I will not discuss here. And from the optimal allocation \\(x\\), we generalise the portfolio to \\(n\\) risky assets then we should be able to draw tangent portfolio, efficient frontier (see the work of Eugene Fama), feasible set etc.

## 4. Markowitz Optimisation Problem

Let's assume we did a great job in analysing efficient frontier and feasible set ;D

Then it rises the following problem proposed by Harry Markowitz: agents want to maximize their expected return of portolio composed by \\(n\\) different shares hence \\(n\\) different allocations \\(x_i\\) such that \\(\sum^n_{i=1}x_i = 1\\), with a target level of risk \\(\tilde{\sigma}^2_P\\) such that \\(\sum^n_{i=1}\sum^n_{j=1}x_ix_i\sigma_{ij} = \tilde{\sigma}^2_P\\). Mathematical formulation: (u/c means under constraint)

$$\begin{cases}
\max_{x_i} E(R_P) = \sum^n_{i=1} x_i E(R_i) \\
u/c: \sum^n_{i=1}\sum^n_{j=1}x_ix_i\sigma_{ij} = \tilde{\sigma}^2_P \\
u/c: \sum^n_{i=1}x_i = 1
\end{cases}$$

which can be reformulated as below:

$$\begin{cases}
\min_{x_i} \sigma^2_P = \sum^n_{i=1}\sum^n_{j=1}x_ix_i\sigma_{ij} \\
u/c: \sum^n_{i=1} x_i E(R_i) = \tilde{E}(R_P) \\
u/c: \sum^n_{i=1}x_i = 1
\end{cases}$$

From this formulation of allocation optimisation problem (basically portfolio diversification problem), Sharpe, Mossin, and Lingtner start modelising the first version of CAPM called **Sharpe-Mossin-Lintner** CAPM.

## 5. Sharpe-Mossin-Lintener CAPM

This model, that I will call **Sharpe CAPM** from now on, allows us to determine the price of financial assets at any moment.

### 5.1 Hypotheses of the model

1. All investors are more or less averse to risk > kinda true
2. All investors have the same time horizon for investment > unrealistic
3. All investors are addressing to the same problem that is **Markowitz Problem**:
  - only way to diversify is to change the allocations
  - all investors anticipate same expected return (gain) and same variance (risk) of portfolio
4. Financial market is a **perfect market**:
  - no tax
  - no transaction cost
  - no asymmetry of information
  - there is a risk-free asset with \\(r_f\\) at which we can borrow and lend capital freely

All these look quite heavy but what you gotto know are two things: **Markowitz problem is in the center**, and **there is a risk-free asset**.

Let's bring back the Markowitz problem but **with a risk-free rate \\(r_f\\). The problem is now written as below:

$$\begin{cases}
\min_{x_i} \sigma^2_P = \sum^n_{i=1}\sum^n_{j=1}x_ix_i\sigma_{ij} \\
u/c: \sum^n_{i=1} x_i E(R_i) + x_0r_f = E(R_P) \\
u/c: \sum^n_{i=1}x_i + x_0 = 1
\end{cases}$$

We combine two constraints into one:

from the second constraint, we get \\( x_0 = 1 - \sum x_i \\). Put it into the first contraint:

$$ \begin{align}
&E(R_P) = \sum x_i E(R_i) + (1-\sum x_i)r_f \\
&E(R_P) - r_f = \sum x_i E(R_i) - r_f\sum x_i + r_f - r_f \\
&E(R_P) - r_f = \sum x_i (E(R_i) - r_f)
\end{align} $$

The last equation means (excess or portfolio return) = sum of each expected return of risky asset diminshed by risk-free return. This result is quite intuitive yet hard to be proven arithematically. **The queation can be transformed into matrix as well**.

Let \\(V\\), var-cov matrix of all returns of size (N,N) and all other terms are as below

$$  \mathbb{R} = \begin{bmatrix} R_1 \\ \vdots \\ R_n \end{bmatrix}
~~~
E = \begin{bmatrix} E(R_1) - r_0 \\ \vdots \\ E(R_n) - r_0 \end{bmatrix}
~~~
X = \begin{bmatrix} X_1  \\ \vdots \\ X_n \end{bmatrix}
$$

Optimisation(minimisation) problem of investors can be written as

$$\begin{cases}

\min_X X^T V X \\
u/c: X^T E = E(R_P) - r_f

\end{cases}$$

Lagrangian optimisation:

$$ \mathcal{L}(X,\lambda) = X^T V X + \lambda(E(R_P)-r_f-X^TE) $$

FOC:

$$ \frac{\delta \mathcal{L}}{\delta X} = 0 ~~~ \iff ~~~ 2VX - \lambda E = 0 $$

$$ X^* = \frac{1}{2}\lambda V^{-1} E $$

This X matrix is the vector of all optimal allocations taking Sharpe ratio as its slope. This is true for all investors.

And at **Equilibirum, the sum of all portfolios of investors must be equal to the market portfolio**. In other words, at equlibirum, the total demand of financial assets is equal to the total supply of financial assets on financial market. Given this parity, at equilibrium, the optimal allocation X can be summed up from both supply and demand thus can be rewritten as

$$ X_M = \lambda_M V^{-1} E $$

where \\(\lambda _M \\) is unknown.

This relation containes both first-order moment and second-order moment anticipations of investors. We now have to determine what is this unknown \\(\lambda _M \\). 

### 5.2 CAPM Formula Induction

**First Big Step:**

- Isolate E.

$$ E = \frac{1}{\lambda_M} V X_M $$

- Multiply \\(X^T\\) at both sides.

$$ X^T E = \frac{1}{\lambda_M} X^T_M V X_M $$

- Focus on the market return excess \\(E(R_M) - r_f \\). Also, \\(X^T_M X\\) will add up to 1. Therefore, \\(X^T_M V X_M \\) is equal to market volatility which is \\(\sigma ^2_M\\):

$$ E(R_M) - r_f = \frac{1}{\lambda_M} \sigma^2_M $$

- Finally we isolate \\(\lambda _M \\)

$$ \lambda_M = \frac{\sigma^2_M}{E(R_M) - r_f} $$

**Second Big Step:**

- Going back to the first step, we isolate E only for a single financial asset.

$$ E(R_i) - r_f = \frac{1}{\lambda_M} \sigma_{iM} $$

- We replace \\(\lambda _M \\) by the result of the **First Big Step**:

$$ E(R_i) - r_f = \frac{1}{\frac{\sigma^2_M}{E(R_M) - r_f}} \sigma_{iM} $$