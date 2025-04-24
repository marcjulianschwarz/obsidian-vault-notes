---
uni-module: "XAI"

alias: "Adjusted R-Squared"
---

# R-Squared

In [[Linear Regression]] is tells us how much of the total [[Varianz|Variance]] of the target outcome is explained by the model.

$$R^2=1-\frac{\sum_{i=1}^n\left(y^{(i)}-\hat{y}^{(i)}\right)^2}{\sum_{i=1}^n\left(y^{(i)}-\bar{y}\right)^2}$$

- $<0$ → worse than mean predictor
- $0$ → mean predictor
- $1$ → best possible score.

## Adjusted

Normal R-Squared gets bigger with more features, so it is better to use the adjusted version:
$$\bar{R}^2=1-\left(1-R^2\right) \frac{n-1}{n-p-1}$$
where $n$ number of datapoints and $p$ number of features.
