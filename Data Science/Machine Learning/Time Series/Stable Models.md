---
uni-module: MBNN
---
# Stable Models

As we work with overparameterized models we have a whole continous manifold of minima. To find a unique minimum we want to focus on modelling **stable** models. 

A model is stable when removing one datapoint from the training set does not have a big impact on the overall gradient distribution. 

In a local minimum we always have a fixed balanced force field of the gradients. If we didn't have this balanced field we could still improve in the direction of the gradients and would therefore not be in a local minimum.

Doing a [[Taylor-Approximation|Taylor Expansion]] we get for [[Stochastic Gradient Descent|Pattern by Pattern Learning]]:
$$\langle E(w)\rangle=\frac{1}{T} \sum_t E\left(w+\Delta_t\right)=E(w)+\frac{\eta^2}{2} \sum_i \operatorname{var}\left(g_{i t}\right) \frac{\partial^2 E}{\partial w_i^2}$$
Here we have a [[Smoothness Penalty]] weighted by the [[Varianz|Variance]] of the [[Gradient|Gradient]] for sample $t$ and weight $i$. So with a high variance gradient we try to enforce smoother weights such that the next gradient will be of less variance.

The same can be done for [[Vario-Eta Learning]]:
$$\langle E(w)\rangle=\frac{1}{T} \sum_t E\left(w+\Delta w_t\right)=E(w)+\frac{\eta^2}{2} \sum_i \frac{\partial^2 E}{\partial w_i^2}$$
where we have a global unconditional penalty. 

