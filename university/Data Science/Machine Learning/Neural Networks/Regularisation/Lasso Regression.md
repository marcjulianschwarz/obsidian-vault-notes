---
uni-module: "XAI"

alias: ["L1", "L1 Regression", "LASSO", "Least Absolute Shrinkage and Selection Operator"]
---

# Lasso Regression

Just like [[Ridge Regression]] it uses a penalty / [[Regularisation]] term to regularise the slope of the [[Regression]] line and performs [[Feature Selection|Feature Selection]].
$$\lambda\mid s\mid$$
where $s$ is the slope.

Minimize the sum of least squares and a penalty or [[Regularisation]] term.

$$\min _\beta\left(\frac{1}{n} \sum_{i=1}^n\left(y^{(i)}-x_i^T \beta\right)^2+\lambda\|\beta\|_1\right)$$

Used to prevent [[Overfitting]].

Also can exclude useless variables/features completely by minimizing their weights (slope) right down to zero. This allows us to do [[Feature Selection|Feature Selection]] and also infer some kind of [[Feature Importance]] from the weight plots:

![[Bildschirm­foto 2023-05-07 um 19.24.50.png]]

In this case the windspeed and humidity dont seem to play such a huge role.
To find the optimal value for lambda use [[K-Fold Cross Validation]].

## Classification

This method also works for [[Logistic Regression]] [[Classification]].

## Explainability

Just like in [[Linear Regression]] with the added benefit of automatic [[Feature Selection|Feature Selection]] and [[Regularisation]].

## Resources

- https://www.youtube.com/watch?v=NGf0voTMlcs
