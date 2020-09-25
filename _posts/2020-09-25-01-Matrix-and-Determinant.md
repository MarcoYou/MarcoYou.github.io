---
layout: post
toc: true
title: "01. Matrix and Determinant"
categories: Linear_Algebra
tags: [linear algebra, matrix, maths]
math: true
author:
  - Marco You
  - Sangyup Lee
[comment]: <> (mathjax inline > \\(...\\) )
[comment]: <> (mathjax block  > $$...$$   )
---

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce bibendum neque eget nunc mattis eu sollicitudin enim tincidunt. Vestibulum lacus tortor, ultricies id dignissim ac, bibendum in velit.

## 1. Matrix

### 1.1 Notions and Definitions

#### Basics

$$ A = \begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{bmatrix} $$

- **elements** : \\(a_{ij}\\) is a certain element located in i-th row and j-th column in a matrix. Here, for example, \\(a_{12}\\) = 2 ;
- **row** : (1 2 3) and (4 5 6) are called rows (there are m = 2 rows) ;
- **column** : (1 4), (2 5), and (3 6) are called columns (there are n = 3 columns) ;
- **matrix size** : A is a m(= 2) by n(= 3) matrix denoted as \\( A(2 \times 3) \\) or in general \\( A(m \times n) \\) ;
- **transposition** : the notation for transpose of the matrix A is \\(A^T\\) or \\(A'\\) and is expressed as below

$$ A^T = A' = \begin{bmatrix} 1 & 4 \\ 2 & 5 \\ 3 & 6 \end{bmatrix} $$

#### Further details

$$ D = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{bmatrix} $$

- D is a **diagonal matrix** and (1 1 1) is the diagonal (or diagonal elements) of D ;
- D is an **identity matrix** which has to contain only 1 as its diagonal elements values. An identity matrix is often denoted as I ;
- D is a **square matrix** (number of rows = number of columns) ;

$$ S = \begin{bmatrix} a & 2 & 3 \\ 2 & b & 4 \\ 3 & 4 & c \end{bmatrix} = S^T$$

- S is a **symetric matrix** which has identical elememnts across the diagonal (elements in the diagnoal do not matter) ;
- A symetric is necessarily a square matrix ;
- Transpose of a symetric matrix is equal to its original matrix \\(S^T = S\\) ;

### 1.2 Matrix Computation

For \\(A(m \times n) = (a_{ij} \\) and \\(B(m \times n) = (b_{ij}) \\), following computations are valid

- Addition and Substration : \\( A ± B = (a_{ij} ± b_{ij}) \\) ;
- Constant factor multiplication : \\( cA = (ca_{ij}) \\) (c is a constant) ;

For \\(A(m \times n) = (a_{ij} \\) and \\(B(n \times r) = (b_{jk}) \\), following computations are valid

- Matrix multiplication : \\( A(m \times n) \times B(n \times r) = AB(m \times r) = (c_{ik}) = \sum_{j=1}^n{a_{ij}b_{jk}} \\) ;
- Matrix multiplication computation is not commutative. Which means \\(AB ≠ BA\\) ;

example)

## 2. First Order Equation System

### 2.1 Another way to express a matrix

A first order equation system (***FOES***) is another way to express and solve a matrix problem. Reciprocally, we can also express a FOSE in terms of matrix and solve it with matrices through two different ways. The first method is **Gauss-Jordan elimination method**,

#### Gauss-Jordan Elimination Method

First we express the given FOES as an **augmented matrix**,

$$ \begin{cases} x + 2y = 5 \\ 2x + 3y = 8 \end{cases} \iff \begin{bmatrix} 1 & 2 & 5 \\ 2 & 3 & 8 \end{bmatrix} $$

then we use one of or a combination of following operations to simplify the matrix as much as possible in a echelon shape :
1. multiply a constant to a row ;
2. add/substract the result of (1) to/from another row ;
3. switch rows ;

$$ \begin{bmatrix} 1 & 2 & 5 \\ 2 & 3 & 8 \end{bmatrix} \implies (r_2 - 2r_1) \implies \begin{bmatrix} 1 & 2 & 5 \\ 0 & -1 & -2 \end{bmatrix} $$

$$ \begin{bmatrix} 1 & 2 & 5 \\ 0 & -1 & -2 \end{bmatrix} \implies (- r_2) \implies \begin{bmatrix} 1 & 2 & 5 \\ 0 & 1 & 2 \end{bmatrix} $$

$$ \begin{bmatrix} 1 & 2 & 5 \\ 0 & 1 & 2 \end{bmatrix} \implies (r_1 - 2r_2) \implies \begin{bmatrix} 1 & 0 & 1 \\ 0 & 1 & 2 \end{bmatrix} $$

The final matrix is called **reduced row echelon matrix** due to its form. With Gauss-Jordan elimination method, we are supposed to simplify all the elements to zeros, ones or if impossible, to prime numbers. The final matrix then can be expressed in FOES as below

$$ \begin{bmatrix} 1 & 0 & 1 \\ 0 & 1 & 2 \end{bmatrix} \implies 
\begin{cases} 1x + 0y = 1 \\ 0x + 1y = 2 \end{cases} \implies
\begin{cases} x = 1 \\ y = 2 \end{cases} $$

The solutions that this method found are \\(x = 1\\) and \\( y = 2\\).

the second method is **Inverse matrix method**.

#### Inverse Matrix Method

With this method, there are two questions to answer. ***"How do we know if the inverse matrix exists ?"*** and then ***"If it does, how do we compute it ?"***.

For a matrix equation \\(AX = B\\), if \\(A\\)'s inverse matrix \\(A^{-1}\\) exists, then \\(X = A^{-1}B\\),




### Tables

Title 1               | Title 2               | Title 3               | Title 4
--------------------- | --------------------- | --------------------- | ---------------------
lorem                 | lorem ipsum           | lorem ipsum dolor     | lorem ipsum dolor sit
lorem ipsum dolor sit | lorem ipsum dolor sit | lorem ipsum dolor sit | lorem ipsum dolor sit
lorem ipsum dolor sit | lorem ipsum dolor sit | lorem ipsum dolor sit | lorem ipsum dolor sit
lorem ipsum dolor sit | lorem ipsum dolor sit | lorem ipsum dolor sit | lorem ipsum dolor sit


Title 1 | Title 2 | Title 3 | Title 4
--- | --- | --- | ---
lorem | lorem ipsum | lorem ipsum dolor | lorem ipsum dolor sit
lorem ipsum dolor sit amet | lorem ipsum dolor sit amet consectetur | lorem ipsum dolor sit amet | lorem ipsum dolor sit
lorem ipsum dolor | lorem ipsum | lorem | lorem ipsum
lorem ipsum dolor | lorem ipsum dolor sit | lorem ipsum dolor sit amet | lorem ipsum dolor sit amet consectetur
