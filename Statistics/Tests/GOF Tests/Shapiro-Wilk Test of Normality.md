---
uni-module: "ISSP"
---

# Shapiro-Wilk Test of Normality

Is a [[qq GOF Test for Class of Distributions]], in this case [[Normalverteilung|Normal Distributions]].

## How to perform the test

Make [[qq-Plot]] for any [[Normalverteilung|Normal Distribution]] against [[Standardnormalverteilung|Standard Normal Distribution]]. Use simple [[Linear Regression]] to fit a diagonal line to the plot and read off the slope $S$.

Calculate [[Test Statistic]]
$$T=\frac{S^2}{s^2}$$
where $s$ is the empirical [[Standardabweichung|standard deviation]] for the data sequence.

Given $H_{0}$ the test statistic will be close to $1$. You can quanitfy this by simulating the test statistic and determening its [[Wahrscheinlichkeitsmaß|distribution]]. You can calculate an [[Acceptance Domain]] with
$$[z_{\alpha / 2}, z_{1- \alpha / 2}]$$
where $\alpha$ is the probability for [[Type 1 Error]].
