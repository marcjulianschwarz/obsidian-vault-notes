---
uni-module: MBNN
---
# Sinus Activation


We can approximate the [[Hyperbolic Tangent|tanh]] function with the non-monotonic sinus function. 

![[CleanShot 2023-11-18 at 22.57.43@2x.png]]

We can rewrite multiplications of sinus functions into sums of sinus functions 
$$\sin (x) \cdot \sin (y)=\frac{1}{2}\left[\sin \left(x-y+\frac{\pi}{2}\right)+\sin \left(x+y-\frac{\pi}{2}\right)\right]$$
which is a nice idea as sums are easier to compute than multiplications.

Also, sinus partly avoids vanishing [[Gradient|Gradients]] in [[Backpropagation]].
