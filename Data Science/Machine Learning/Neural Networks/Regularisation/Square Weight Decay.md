---
uni-module: MBNN
---
# Square Weight Decay

Square Weigth Decay is a [[Regularisation]] method that enforces small weights and thus has a prior towards linear models as the weight values are in the linear range of the [[Hyperbolic Tangent|tanh]] function. 

It works by adding the squared weights to the error function. Minimizing the error will also lead to smaller weights.

$$E(w)=E_0(w)+\lambda \sum_w \frac{1}{2} w^2 \rightarrow \min _w$$

$$w_{+}=(1-\lambda) w-\eta \frac{\partial E_0(w)}{\partial w}$$

A small weight decay will sort out completely unneeded weights. This method is similar to [[Lasso Regression|LASSO]] where the end result is a kind of [[Feature Selection]].
