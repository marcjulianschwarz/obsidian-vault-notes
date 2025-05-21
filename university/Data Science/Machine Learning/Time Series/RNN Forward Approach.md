
# RNN Forward Approach

An approach to model a [[Recurrent Neural Network]] based on a [[State Space Model]] where the *current* state is being used to calculate the next state.  So it takes at least one more time step to see the effect in the observations.
$$\begin{gathered}
s_{t+1}=f\left(s_t, u_t\right) \\
y_t=g\left(s_t\right)
\end{gathered}$$
We can translate this [[Stetigkeit|continous]] model to a [[Neural Network]] structure via universal approximation:

![[Bildschirm­foto 2023-04-11 um 23.15.26.png]]

## Architecture 

- Allows to include $y_t$ as input 
- Shift along the time labeling

![[Bildschirm­foto 2023-04-11 um 23.19.26.png]]
