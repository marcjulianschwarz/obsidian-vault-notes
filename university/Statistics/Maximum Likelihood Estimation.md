---
uni-module: EMD
aliases:
  - MLE
  - ML Learning
---
# Maximum Likelihood Estimation

From all possible $\phi$ parameters we will select the ones which most likely generated the training set. (selecting the maximum depending on the [[Dataset]])
$$\underset{h_i}{\arg\max}\quad P(d\mid h_i)$$
= [[Maximum A Posteriori Learning|MAP Learning]] for a uniform [[Prior Probability|Prior]].

This method uses the [[Log-Likelihood]] function. It has to be maximized to get to its minimum (negative sign).

Solve with [[Newton Verfahren|Newton Method]]:

So we have:

$$\theta^{k+1}=\theta^k-\nabla^2L(\theta^k)^{-1}\nabla L(\theta^k)$$
So basically current parameters minus inverse of the [[Hessematrix|hessian matrix]] times the [[Gradient]].

One can use different methods to calculate the minimum:

- [[Gradient Descent]]
- [[Newton Verfahren|Newtons Method]]
- Analytical solution
