---
uni-module: "MBNN"
---
# Sensitivity Analysis

This type of analysis can be used to do [[Feature Selection|Feature Selection]] for a [[Neural Network]] by looking at how big the influence of a tiny change in one input variable has on the output of the very first prediction.

$$\frac{\partial y_t}{\partial u_{\tau \leq t}}$$

There are four possibley types of relations 
- linear with constant first derivative 
- monotone, can be used in one dimensional control 
- non-monotone, can only be used in multi-dimensional control 
- near zero, useless for modelling and control 

