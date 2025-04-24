---
uni-module: EMD

alias: "Lineare Regression"
---

# Linear Regression

Predicts the target as a weighted sum of the feature inputs.

## Assumptions

- Linearity (no interactions and no non-linearities)
- Normality (target variable follows a [[Normalverteilung|Normal Distribution]] given the features)
- [[Homoscedasticity]]
  - e.g. high house price variance vs. low house price variance
- [[stochastisch unabhängig|Independence]]
  - if not, use Mixed Effect Model or GEEs
- Fixed Features (there is no measurement error or uncertainty in the data)
  - otherwise a more complex model has to be used to account for the possible measurement error
- Uncorrelated Features ([[Korrelation|Correlation]])
  - it becomes hard to know which feature of the correlated ones is having the effect on the target
  - use [[Linear Discriminant Analysis|LDA]] to get less correlated features

## Problem to solve

Given some datapoint $x$ with targets $y$, find weights $\beta$ that minimize the error $\epsilon$.

$$
\begin{gathered}
y=\beta_0+\beta_1 x_1+\ldots+\beta_p x_p+\epsilon \\
\hat{\boldsymbol{\beta}}=\underset{\beta_0, \ldots, \beta_p}{\arg \min _{i=1}} \sum^n\left(y^{(i)}-\left(\beta_0+\sum_{j=1}^p \beta_j x_j^{(i)}\right)\right)^2
\end{gathered}
$$

There is a closed form solution (see below) or you can use [[Gradient Descent]] to calculate the weights from minimizing the [[Mean Squared Error]].

If our data has [[Normalverteilung|Gaussian]] noise we can even get confidence intervals for beta.

## Explanations

Linear Regression has [[Ante-Hoc|Intrinsic]] explanations.

We can get [[Explanation|Explanations]] from a Linear Regression model via the estimated weights.

- Numerical
  - one unit change → outcome changes by its weight
- Binary
  - changing from 0 to 1 → outcome changes by weight
- Categorical
  - [[One-Hot-Encoding]] → Binary
- Intercept
  - Predicted value when all values are at their mean (when standardized)
  - else when all values are zero

[[Feature Importance]] can be calculated with the [[t-Distribution|t-statistic]].
$$t_{\hat{\beta}_j}=\frac{\hat{\beta}_j}{S E\left(\hat{\beta}_j\right)}$$
So the importance increases when the weight of the feature increases and it decreases when it is uncertain about the correct value.

We can plot the importances with a [[Weight Plot]] and the features [[Effect (XAI)|Effects]] with an [[Effect Plot]].

### Quality of Explanations

- [[Contrastive]]
  - to the zero values instance
  - or the mean values instance (when normalized)
- [[Fidelity]]
  - Explanations are truthful if the assumptions are held
  - otherwise it might simplify the actual dependencies to simple linear dependencies which of course then are not truthful
- [[Stability]]
  - Stable by design
- Not [[Selectivity|selective]] by default
  - [[Feature Selection|Feature Selection]] might be necessary
  - [[Feature Engineering]] might be necessary when there are non-linearities

## Evaluation

To evaluate a linear regression model, one can use the [[R-Squared]] [[Metrik|Metric]].

## Disadvantages

All nonlinearities have to be hand-crafted and given as input features. Sometimes weights are not interpretable when you have high correlation (e.g. room number and size of house).

## Other

What model describes our data the best?

- [[Linear Model]]
- [[Linear Gaussian Model]]
- [[Exponential Growth]]
- [[Allometric Growth]]

### Simple Linear Regression

A calculation with the [[Linear Gaussian Model]] yields a solution to the simple linear regression if not all datapoints are the same.
$$\widehat{\gamma_1}=\frac{c(\boldsymbol{x}, \boldsymbol{t})}{V(\boldsymbol{t})}$$
$$\widehat{\gamma_0}=M(\boldsymbol{x})-\widehat{\gamma_1} M(\boldsymbol{t})$$

or, in terms of the data 

$$\mathrm{w}_1=\frac{N\left(\sum_j x_j y_j\right)-\left(\sum_j x_j\right)\left(\sum_j y_j\right)}{N\left(\sum_j x_j^2\right)-\left(\sum_j x_j\right)^2} \quad \mathrm{w}_0=\frac{\left(\sum_j y_j\right)-\mathrm{w}_1\left(\sum_j x_j\right)}{N}$$

The _regression line_ is defined as
$$t \mapsto \widehat{\gamma_0}+\widehat{\gamma_1} t$$
which goes through the [[Center of Mass]] of the data sequence.

[[Empirical Correlation Coefficient]]

### Steps

1. [[Linear Model]]
2. [[Optimization of a Linear Model]]
3. [[Basis Function Expansion]]

### Use Cases for Linear Regression

- Computer vision and trend analysis.
- [[Dataset]] is rather small and a [[Linear Model]] is enough to approximate the function.
- We use regression to predict a real-valued output.

### Class Prediction

By applying [[Logistic Regression]] we can also do [[Classification]].
