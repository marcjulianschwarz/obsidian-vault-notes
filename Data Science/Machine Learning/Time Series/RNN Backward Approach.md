---
uni-module: "MBNN"
---

# RNN Backward Approach

An approach to model a [[Recurrent Neural Network]] based on a [[State Space Model]] where the _previous_ state is being used to calculte the new current state.

$$
\begin{gathered}
s_t=f\left(s_{t-1}, u_t\right) \\
y_t=g\left(s_t\right)
\end{gathered}
$$

This approach might be more appropriate when applied to monthly data as we then need to get predictions early and not after the month.

We can translate this [[Stetigkeit|continous]] model to a [[Neural Network]] structure via universal approximation:

![[Bildschirm­foto 2023-04-11 um 23.15.10.png]]

## Architecture

- Allows regular time labeling (see that index is always the same per layer)
- Disallows to include $y_1$ as input

![[Bildschirm­foto 2023-04-11 um 23.18.09.png]]
