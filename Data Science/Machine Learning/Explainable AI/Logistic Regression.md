---
uni-module: "XAI"
---

# Logistic Regression

Logistic Regression is a [[Classification]] [[Machine Learning|ML]] model. It is the application of [[Linear Regression]] to classification by feeding the output of the [[Linear Regression]], the so called [[Log Odds]] into the [[Logistic Function|Sigmoid Function]] to get class probabilities.

> Regression of the parameter of a binary random variable (y).

$$P\left(y^{(i)}=1\right)=\frac{1}{1+\exp \left(-\left(\beta_0+\beta_1 x_1^{(i)}+\ldots+\beta_p x_p^{(i)}\right)\right)}$$

We can interpret the output as a **probability** which is really nice for [[Explainability]] purposes. So for a [[Binary Classification]] we can choose 0.5 as a probability threshold for the two classes.

It uses [[Gradient Descent]] to find the [[globales Minimum|global minimum]] of the [[Log-Likelihood]].

The logistic update is 

$$\mathrm{w}_i \longleftarrow \mathrm{w}_i+\alpha \cdot\left(y-h_{\mathrm{w}}(\mathrm{x})\right) \cdot h_{\mathrm{w}}(\mathrm{x}) \cdot\left(1-h_{\mathrm{w}}(\mathrm{x})\right) \cdot x_i$$

## scikit-learn

You can use the argument `multi_class="multinomial"` to get a multiclass [[Classification]].

You can use the argument `C` which is inversly proportional to the [[Regularisation]] parameter. So you can perform a kind of [[Ridge Regression|L2 shrinkage]] to penalize large weights ([[Overfitting]]).

## Explanations from Logistic Regression

See [[Log Odds|Odds Ratio]] for how to explain outcomes by increases in features.

- Numerical
  - increase by one unit → changes odds **multiplicatively** by exp(weight)
- Binary
  - same
- [[Categorical Data]]
  - [[One-Hot-Encoding]] → same
- Intercept
  - same

## Problem of complete separation

If a feature can perfectly separate the classes, the logistic regression will not converge (because infinite weights would be needed).∑

→ Use [[Regularisation]]
→ Or just use a rule based approach and not ML

## Calculating Odds by Hand

![[Bildschirmfoto 2023-07-26 um 11.30.06.png]]
