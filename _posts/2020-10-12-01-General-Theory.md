---
layout: post
toc: true
title: "01. General Theory"
categories: Risk_Theory
tags: [risk, probability, statistics, utility, insurance, information]
math: true
author:
  - Marco You
  - PSE lectures
[comment]: <> (mathjax inline > \\(...\\) )
[comment]: <> (mathjax block  > $$...$$   )
---

In the General Theory of risk, known as Expected Utility Theory developed by Von Neumann and Morgenstern in 1947 (***Theory of Games and Economic Behavior***), only consequences matter (the process and the framing do not matter). The choices made by the agent may affect consequences that are often monetary consequences.

## 1. Expected Utility Model (EUT)

### 1.1 Lotteries

Two types of information are necessary to describe a **risky environment** :

- **enumeration of all possible outcomes**
  - Set of all possible outcomes (often monetary consequences) that affect the well-being of the decision maker
  - Such set is assumed to be finite ;
- **characterization of the risky environment**
  - Probability vector of the possible outcomes,
  - \\( p_s \\) = probability of outcome \\( s \\) occurring, with \\( \sum{p_s} = 1\\) ;

#### Definition
A **lottery** \\(L\\) is a vector of probabilities \\( (p_1, \dots, p_s) \\). A lottery can aslo be written as a real random variable X, in other words, it is a function that maps the states of the world into \\( \Bbb{R} \\).

#### Definition
The **utility function** \\( U:\mathcal{L} \rightarrow \Bbb{R} \\) has, under the Expected Utility Theory, an expected utility form if there is an assignment of numbers \\( (u_1, \dots, u_n) \\) to the n outcomes such that for every simple lottery \\( L = (p_1, \dots, p_n) \in \mathcal{L} \\) we have :

$$ U(L) = u_1p_1 + \dots + u_np_n $$ 

A utility function U with the expected utility form is called a **VNM Expected Utility Function**. (***VNM for Von Neumann-Morgenstern***)

### 1.2 Axioms

The underlying assumption behind the VNM Expected Utlity Theory is "***if a person's preferences satisfy the following axioms, then he or she should choose between lotteries by using the expected utility criterion***."

- **Axiom 1 (Completeness)** : For any lotteries X and Y, one of the following three binary relations should be held :
  - \\( X \succ Y \\) : X is preferred over Y,
  - \\( Y \succ X \\) : Y is preferred over X,
  - \\( X \sim Y \\) : indifferent between X and Y ;
- **Axiom 2 (Transitivity)** : For any lotteries X, Y, and Z, the preference over these lotteries is well-ordered :
  - If \\( X \succ Y \\) and \\( Y \succ Z \\) then \\( X \succ Z \\),
  - If \\( X \sim Y \\) and \\( X \sim Y \\) then \\( X \sim Y \\) ;
- **Axiom 3 (Continuity)** : For any lotteries X, Y, and Z,
  - If \\( X \succ Y \succ Z \\), then there is a unique probability \\(p \in ]0;1[ \\) such that \\(pX + (1-p)Z \sim Y \\) : (small probability of best outcome) + (big probability of worst outcome) is indifferent to sure middle outcome,
  - or, if \\( X \succ Y \succ Z \\), then there is a unique probability \\(\pi \in ]0;1[ \\) such that \\((1-\pi)X + \pi Z \succ Y \succ \pi X + (1-\pi) Z\\) : this is called Archimedean property.
  - only one of two properties above needs to be assumed in order to support the VNM-EUT.
- **Axiom 4 (Independence)** : For any lottery X,Y, and Z and probability \\( p \in ]0;1[\\),
  - If \\( X \succ Y \\), then \\(pX + (1-p)Z \succ pY + (1-p)Z \\) : (better outcome + unknown outcome) is preferred to (worse outcome + same unknown outcome)
  - This axiom implies that we can always express a simple lottery as a compound lottery and vice versa
  - This axiom also implies that the preference function U must be linear in probabilities : \\( U(L) = \sum_{i=1}^n{p_i u_i} \\)
  - This axiom is the most controversial point of EUT and the most violated axiom of the EUT.

### 1.3 Theorem

#### Expected Utility Theorem

For any lotteries X and Y, \\( X \succeq Y \implies \sum{p^x_iu_i} ≥ \sum{p^y_iu_i}  \\)

## 2. Risk Aversion

### 2.1 Characterization
### 2.2 Comparison in Risk Aversion

## 3. Changes in Risk

### 3.1 Second Order Stochastic Dominance (SOSD)
### 3.2 First Order Stochastic Dominance (FOSD)
### 3.3 Other Risk Measures