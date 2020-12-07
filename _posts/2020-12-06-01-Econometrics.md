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

### 1.1 Random Variable

**Simple Definition**

**Random variable** X is a variable whose value is determined by the outcome of a random experiment.

Therefore, a random variable X needs following elements:

- \\( x_1, x_2, \cdots, x_k \\) (k possible outcomes)
- \\( p_1, p_2, \cdots, p_k \\) (probability of each outcome)
- \\( \{x_1, x_2, \cdots, x_k\} \\) (sample space)

where \\(p_i ≥ 0 \\) and \\( \sum^k_{i=1} p_i = 1 \\).

**Fancy Definition**

In formal mathematical terms, we can also say that a random variable is a function defined on a probability space that maps from the sample space to the real numbers, where

- Probability space \\(\equiv (\Omega, \mathcal{F}, \mathbb{P}) \\) where
  - Sample sapce \\(\equiv \Omega \\) is a non-empty set of all possible outcomes (numbers) or results (not numbers) from a random experiment.
  - \\(\sigma\\)-algebra \\(\equiv \mathcal{F}\\) is a set of all possible subsets of \\(\Omega\\), called events. 
  - Probability measure \\(\equiv \mathbb{P}\\) is a function that maps from \\(\sigma\\)-algebra to a probability \\(p \in \[0,1\]\\).

$$ \begin{align}
&\Omega = \{\omega_1, \omega_2 \} \\
&\mathcal{F} = \{\emptyset, \{\omega_1\}, \{\omega_2\}, \{\omega_1, \omega_2\} \} \\
&\mathbb{P}(\emptyset) = p_0 = 0 \\
&\mathbb{P}(\{\omega_1\}) = p_1 = 0,50 \\
&\mathbb{P}(\{\omega_2\}) = p_2 = 0,50 \\
&\mathbb{P}(\{\omega_1, \omega_2\}) = \mathbb{P}(\Omega) = p_3 = 1,00
\end{align}$$

**Random Variable Types**

Outcomes of a random variable could either be **discrete** or **continuous**. In the first case, the outcomes are numerable. In the second case, the outcomes are not numerable.

### 1.2 Probability Distribution Function

For any random variable X one can define its **Probability Distribution Function**. It is a function of stacked probabilities of each possible value of X when it occurs. There are two types of probability distribution function that are **Probability Mass Function** and **Probability Density Function**.

#### 1.2.1 Probability Mass Function

When X is a **discrete random variable**, we use **Probability Mass Function** (PMF). PMF is defined as such:

Let X be a discrete random variable defined as \\(X:\Omega \mapsto \mathbb{R} \\). Then the probability mass function of X is defined as:

$$ \begin{align} 
PMF(X) \equiv f_X(x) &= P(X=x) \\ 
&= P(\{\omega \in \Omega: X(\omega) = x\})
\end{align} $$

This gives the **probability that a discrete random variable X is exactly equal to some value x**. You will see right after that this is impossible with continuous random variable.

#### 1.2.2 Probability Density Function

When X is a **continuous random variable**, we use **Probability Density Function** (PDF). PDF is defind as such:

Let X be a continuous random variable defined as \\(X:\Omega \mapsto \mathbb{R} \\). Let's denote the probability density function of X, \\PDF(X) \equiv (f_X(x)\\). Given this, probability is computed by:

$$ P(a ≤ X ≤ b) \int^b_a{f_X(x)dx} $$

where \\( f_X(x) ≥ 0 \\) and \\( \int^{+\infty}_{-\infty}{f_X(x)dx} = 1 \\).

This gives the probability of X falling within the infinitesimal interval \\(\[a,b\]\\). 

However, the probability of X being exactly equal to a certain value is 0 when X is a continuous RV. Intuitively we know that it's because we have continuous real numbers that can be infinitesimally refined to extremely and infinitely small numbers. But this explanation does not sound mathematically beautiful.

Let's think in this way: we just said the formula above gives the probability of X falling within the interval \\(\[a,b\]\\). And we know that the formula with integral gives the area below curve \\( f_X(x) \\). Trying to find a probability of X is exactly equal to a certain value would mean it is a probability of X falling within the interval, for instance, \\(\[a,a\]\\). This is not an area below the curve f. It is a line below the curve f. And what is the area of a line? it's 0. A line has a length but not an area.