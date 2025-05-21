---
uni-module: AI
aliases:
  - Smoothing
  - Hindsight
---
# Markov Smoothing

A type of [[Markov Inference]] for estimating past states via all of the given evidence (essential for learning, why?). 
$$\mathrm{P}\left(\mathrm{X}_k \mid \mathrm{e}_{1: t}\right) \text { for } 0 \leq k<t$$
It works similar to [[Markov Filtering|Filtering]] where you go through all of the evidence iteratively with recursion. Here however the recursion is backwards and goes from the current state to a past state. Of course the past state must not be the first state, so we also do [[Markov Filtering|Filtering]] to get the forward part. 

$$\mathrm{P}\left(\mathrm{X}_k \mid \mathrm{e}_{1: t}\right)=\alpha \cdot f_{1: k} \cdot b_{k+1: t}$$

**The backward message**

$$b_{k+1: t}=P\left(e_{k+1: t} \mid X_k\right)$$
$$=\sum_{\mathrm{x}_{k+1}} P\left(\mathrm{e}_{k+1} \mid \mathrm{x}_{k+1}\right) \cdot P\left(\mathrm{e}_{k+2: t} \mid \mathrm{x}_{k+1}\right) \cdot P\left(\mathrm{x}_{k+1} \mid \mathrm{X}_k\right)$$
We get 
$$P\left(e_{k+1} \mid x_{k+1}\right)$$
by the [[Sensor Model]]. And 
$$\mathrm{P}\left(\mathrm{x}_{k+1} \mid \mathrm{X}_k\right)$$
by the [[Übergangsmatrix|Transition Model]].

The recursive call
$$P\left(\mathrm{e}_{k+2: t} \mid \mathrm{x}_{k+1}\right)$$
goes one more step into the past.