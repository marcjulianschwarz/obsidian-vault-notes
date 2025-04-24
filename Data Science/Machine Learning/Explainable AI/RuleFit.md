---
uni-module: "XAI"
---

# RuleFit

A combination of [[Linear Regression]] and [[Decision Tree]]. This will let [[Linear Regression]] also use interactions between features which it can't on its own.

## Algorithm

1. Fit many random depth [[Decision Tree|decision trees]] and extract rules (paths)
2. Add extracted rules as new (binary) features that can either be fullfilled (1) or not (0)
   1. Clip original features on corresponding [[Perzentil|Quantile]]
   2. [[Z-score|Standardize]] clipped features to be on same scale as the binary rule features
3. Fit [[Lasso Regression|LASSO]] on new feature matrix

## Explainability

As the output of RuleFit is a [[Linear Regression]] model, we can just use its interpretation of the weights of the original features.

For the new features we can calculate the importance using

$$I_k=\left|\hat{\alpha}_k\right| \cdot \sqrt{s_k\left(1-s_k\right)}$$
where
$$s_k=\frac{1}{n} \sum_{i=1}^n r_k\left(x^{(i)}\right)$$
is the rule support for rule $r_k$ and $\hat{\alpha}_k$ is the [[Linear Regression]] weight.

So to get the [[Feature Importance]] for exactly one datapoint ([[Local Explanation]]) we calculate
$$J_j(x)=I_j(x)+\sum_{x_j \in r_k} I_k(x) / m_k.$$
To get a [[Global Explanation]] for a feature we can sum over all datapoints.

$$J_j(X)=\sum_{i=1}^n J_j\left(x^{(i)}\right).$$

## Resources

There are many other methods in the [[Python]] package _imodels_.
