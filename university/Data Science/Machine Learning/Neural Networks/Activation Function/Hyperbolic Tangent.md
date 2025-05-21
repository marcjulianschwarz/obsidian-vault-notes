---
uni-module: MBNN
aliases:
  - tanh
---
# Hyperbolic Tangent

The tanh analyzes diversity in the input space similar to [[Support Vector Machine|SVMs]]. This scales well to high dimensional spaces where tanh does a multidimensional diversity analysis. 

$$\begin{aligned}
y & =\tanh \left(\sum_i w_i x_i-w_0\right) \\
& =\tanh (w \cdot(x-b)) \quad \text { Hessian normal form } \\
& =\tanh (\|w\| \cdot\|x-b\| \cdot \cos \varphi) \\
& =\tanh (\|w\| \cdot \operatorname{dist}(x, \text { hyperplane })) \rightarrow \pm 1
\end{aligned}$$
Here we use the Hessian Normal Form to rewrite the sum into a dot product. We can calculate $b$ to be $\frac{w_0}{w_i}$.
Then we can use the normal dot product rule to rewrite it into the product of the two magnitudes multiplied by the angle between them. Here we can first see that the result of the neuron depends both on the distance to the bias and the angle between the weight and the input. Geometrically we can view it like this:

![[CleanShot 2023-11-18 at 16.05.10@2x.png]]

Multiple dimensions:
$$y=\sum_j v_j \cdot \tanh \left(\sum_i w_{j i} x_i-w_{j 0}\right)$$
Approximate [[Normalverteilung|Normal Distribution]] 
$$y=\sum_j v_j \tanh \left(\sum_i w_{j i} x_i+\mathrm{u}_{\mathrm{ji}} \mathrm{x}_{\mathrm{i}}^2-w_{j 0}\right)$$
when $u$ is not zero the network can also model with [[Radial Basis Function Kernel|RBFs]].

## First Derivative 
$$\tanh ^{\prime}(\text { netin })=1-(\tanh (\text { netin }))^2$$

## Simplifications 

The following simplification is an easy to compute approximation of the tanh function. But it is non-differentiable in two points and we multiply the error flow with zero when leaving the middle range.

In [[Backpropagation]] we have 
$$\left.\partial=f^{\prime}(\text { netin }) d e v\right)$$
which would be zero.
![[CleanShot 2023-11-18 at 22.59.58@2x.png]]


The following two approximations are quite similar to tanh, they all go through the origin and are easier to compute. 
But you can see that the curvature of the functions is slower growing, thus the model will try to learn bigger weights to reach the entire -1, +1 interval.
In generalization this will lead to an unstable model as small changes in the input data will be amplified by the large weights.

$$f(x)=\tanh (x) \quad f_1(x)=\frac{x}{1+|x|} \quad f_2(x)=\frac{x}{\sqrt{1+x^2}}$$
![[CleanShot 2023-11-18 at 23.00.24@2x.png]]
