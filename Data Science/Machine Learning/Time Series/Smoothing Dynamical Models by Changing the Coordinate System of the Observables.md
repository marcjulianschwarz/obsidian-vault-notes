# Smoothing Dynamical Models by Changing the Coordinate System of the Observables

We now looked at ways to either decrease or increase the dimensions of our observable to improve learning. 
Now it might also make sense to use more general coordinate system transformations that optimize for a low curvature on the transformed values to make modelling easier. 

We split this process into two phases.
**Phase 1**
Search for an unfolding (transformation) $g$ and folding (inverse) $h$ such that the difference $\left\|y_t-h \circ g\left(y_t\right)\right\|$  is being minimized with the side constrained that $x_t=g(y_t)$ is **smooth** over time. 

**Phase 2**
Search dynamics in the transformed data such that the difference $\left\|y_t-h \circ f \circ g\left(y_{t-1}\right)\right\|$ is being minimized. 


To find good unfoldings $g$ we need a concept of smoothness in the transformed space. 

We thus use the difference between two transformed values to calculate the change in slope over time. This is also called the [[Smoothness Penalty]]. If it is between zero and one we consider the transformation as smooth. 

![[Bildschirm­foto 2023-06-08 um 13.28.45.png]]

