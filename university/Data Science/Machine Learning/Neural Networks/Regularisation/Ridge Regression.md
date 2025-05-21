---
uni-module: "XAI"

alias: ["L2", "L2 Regression"]
---

# Ridge Regression

Used to prevent [[Overfitting]] and works best when there are few useless features and lots of useful ones (as it will not remove any of them completely). Otherwise, might want to have a look at [[Lasso Regression]].

## Applied to Linear Regression

Ridge Regression is a form of [[Regression]] (in this case [[Linear Regression]]) where a small amount of [[Bias]] is added to the training data. This way the fit to the training data will be slightly worse, but it will provide better generalisation (less [[Varianz|Variance]]) und thus better long term predictions.

It works by adding a penalty / [[Regularisation]] term that has to be minimized while training. It is
$$\lambda s^2$$
where $s$ is the slope of the [[Regression]] line.

What value should $\lambda$ be?
Try out different values and use [[K-Fold Cross Validation]] to determine which one has the best validation score.

## Applied to Logistic Regression

Ridge Regression can also be applied to [[Logistic Regression]] to prevent [[Overfitting]].

## Used when only few datapoints are available

## Resources

- https://www.youtube.com/watch?v=Q81RR3yKn30
