---
aliases:
  - SGD
  - Iterative Gradient Descent
  - IGD
  - Online Gradient Descent
  - OGD
  - Pattern by Pattern Learning
---
# Stochastic Gradient Descent

A [[Gradient Descent]] algorithm that does weight updates for each training sample. The weight update rule is 
$$\Delta w_t=-\eta g_t$$
where 
$$g_t=\frac{\partial E_t}{\partial w}.$$
Over one epoch SGD accumulates to [[Full-Batch Gradient Descent]].

We can rewrite the update rule to
$$\Delta w_t=-\eta g_t=-\eta g \quad-\eta\left(g_t-g\right).$$
Here we can see that we essentially have [[Full-Batch Gradient Descent]] but we subtract some stochastic values in each iteration. 

An approximation of SGD is called [[Vario-Eta Learning]].

## Advantages 

- It converges faster because of more frequent weight updates
	- especially for redundant data
- SGD can escape shallow local minima by stochasticity
- This method can be used to do [[Online Learning]] by partially updating the weights for a new training sample.

