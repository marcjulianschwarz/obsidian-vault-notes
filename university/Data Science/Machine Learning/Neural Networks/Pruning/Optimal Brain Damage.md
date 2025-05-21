---
uni-module: MBNN
aliases:
  - OBD
---
# Optimal Brain Damage

We assume that we have found the minimum of an error function of a [[Neural Network]] and want to determine which weights play an important role. This might be necessary when we want to prune some of the weights.

We shift a given weight to zero and see how much this effects the error function. 

![[CleanShot 2023-12-13 at 17.29.26@2x.png]]

From this, we can formulate the following tests with the distance and curvature
$$E(0)-E(w)=\frac{1}{2} \frac{\partial^2 E}{\partial w^2} w^2$$

