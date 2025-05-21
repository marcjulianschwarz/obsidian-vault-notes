---
alias: ["LDA", "Fisher's LDA"]
---
# Linear Discriminant Analysis

A [[Supervised Learning]] type of [[Dimensionality Reduction]]. It takes class labels into account.

It tries to find the feature subspace that optimizes class separability.

## Assumptions 

- [[Normalverteilung|normally distributed]]
- identical [[Kovarianz|Covariance]] matrices 
- [[stochastisch unabhängig|independent]]

but still works reasonably well with slight violations of these assumptions. 

## General Idea 

![[lda.webp]]

## Steps 

1. [[Z-score|Standardization]]
2. d-dimensional mean vector for every class 
3. Between-Class Scatter Matrix and Within-Class Scatter Matrix 
4. [[Eigenvektor|Eigenvectors]] and [[Eigenwert|Eigenvalues]] for $S_W^{-1}S_B$
5. Sort 
6. Choose top k and create transformation matrix 
7. Project into subspace with transformation matrix 

