---
uni-module: "MBNN"
---

# State Space Model

If we interpret a _dynamical system_ as a state space model we can think of continous functions
$$\frac{ds(t)}{dt}=f(s(t), u(t))$$
, the state transition function and
$$y(t)=g(s(t))$$
a function that observes the current state and returns an [[Entity|Observation]].

- $u$ → external factors
- $s$ → state
- $y$ → observations

![[Bildschirm­foto 2023-04-11 um 23.11.23.png]]

If $u$ experiences some kind of shock, then this will have the possibility to first propagate a few times through the network via $s$ before it becomes visible in $y$. In the original [[Feed-forward Neural Network]] it would directly affect the outputs.

## RNN

One can model a [[State Space Model]] using [[Recurrent Neural Network|RNNs]] in two ways:

- [[RNN Backward Approach]]
- [[RNN Forward Approach]]

When there is only a small timespan between individual time steps, then the two approaches will be quite similar.
