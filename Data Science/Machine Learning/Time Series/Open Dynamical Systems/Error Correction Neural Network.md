---
uni-module: "MBNN"

alias: "ECNN"
---
# Error Correction Neural Network

A [[Recurrent Neural Network]] that uses the forecast error in the current time step as an additional input for the next time step. This should give a hint at how the network might need to change to react to the error.

This error substitutes the unknown external information.

## Equations

$$
\begin{aligned}
& s_t=f\left(s_{t-1}, u_t,\left(y_{t-1}-y_{t-1}^d\right)\right) \\
& y_t=g\left(s_t\right) \\
& \sum_{t=1}^T\left(y_t-y_t^d\right)^2 \rightarrow \min _{f, g}
\end{aligned}
$$

## Architecture

![[Bildschirm­foto 2023-04-14 um 18.15.40.png]]

Alternative

![[Bildschirm­foto 2023-04-18 um 09.57.29.png]]


## Why 

One downside that we currently have with the [[Recurrent Neural Network|RNN]] approach is that for future predictions we don't have any external factors and even for the past we will never get all external factors or even know all external influences. So instead of finding all of these factors we try to at least let the error that was produced by them flow through the network.