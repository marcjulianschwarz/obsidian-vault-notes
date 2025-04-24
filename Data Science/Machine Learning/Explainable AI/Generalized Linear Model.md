---
uni-module: "XAI"

alias: "GLM"
---

# Generalized Linear Model

Extensions for the classical [[Linear Regression]] / [[Linear Model]].

$$g\left(E_Y(y \mid x)\right)=\beta_0+\beta_1 x_1+\ldots \beta_p x_p$$

In [[Logistic Regression]] we for example assume a [[Bernoulli-Verteilung|Bernoulli Distribution]] and use the [[Log Odds|Logit Function]] as the link function.

The probability function can be from the [[Exponential Family]] of [[Wahrscheinlichkeitsmaß|Distribution]] functions.
The link function tries to link the [[Linear Regression]] output with some parameters from the chosen [[Wahrscheinlichkeitsmaß|Distribution]] (e.g. [[Arithmetic Mean|Mean]] and [[Varianz|Variance]]).

- Categorical ([[Bernoulli-Verteilung|Bernoulli Distribution]])
- Count ([[Poisson Verteilung|Poisson Distribution]])
- Duration ([[Exponentialverteilung|Exponential Distribution]])

Trained using [[Maximum Likelihood Estimation]].

## Example

[[Logistic Regression]] is a GLM with [[Bernoulli-Verteilung|Bernoulli Distribution]] and [[Logistic Function]] as link function.

One more example where we chose the [[Poisson Verteilung|Poisson Distribution]] to not get negative values.

![[Bildschirmfoto 2023-07-26 um 11.37.57.png]]

## Interpretation of the weights

Example where the [[Poisson Verteilung|Poisson Distribution]] was used with the log link function.
$$\ln (E(\operatorname{coffee} \mid \operatorname{str}, \mathrm{slp}, \mathrm{wrk}))=\beta_0+\beta_{\mathrm{str}} x_{\mathrm{str}}+\beta_{\mathrm{slp}} x_{\mathrm{slp}}+\beta_{\mathrm{wrk}} x_{\mathrm{wrk}}$$
Apply the inverse of the link function to get the effect on the actual expected outcome.
$$E(\operatorname{coffee} \mid \operatorname{str}, \mathrm{slp}, \mathrm{wrk})=\exp \left(\beta_0+\beta_{\mathrm{str}} x_{\mathrm{str}}+\beta_{\mathrm{slp}} x_{\mathrm{slp}}+\beta_{\mathrm{wrk}} x_{\mathrm{wrk}}\right)$$
