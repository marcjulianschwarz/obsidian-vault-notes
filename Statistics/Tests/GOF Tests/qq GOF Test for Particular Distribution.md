---
uni-module: "ISSP"
---

# qq GOF Test for Particular Distribution

Test if some data comes from a **particular** continous [[Wahrscheinlichkeitsmaß|distribution]] $G$.
$$H_{0}:F=G$$
We know that given $H_0$ the [[qq-Plot]] wil approximately resemble a straight diagonal line which is why we can use the slope of the regression line $T$ as [[Test Statistic]].

The simulated distribution of $T$ on $H_0$ can be used to calculate the [[p-Value]] and [[Acceptance Domain]]:
$$p(t)=2 \cdot \min \{\mathbb{P}(T \leq t), \mathbb{P}(T \geq t)\}$$
$$t \in\left[z_{\alpha / 2}, z_{1-\alpha / 2}\right]$$

This is basically the same as a two [[Two-Sided Gauß Test]].

If we need to accept the [[Null Hypothesis]] the [[Type 2 Error]] cant be quantified without further assumptions for the other hypothesis.
