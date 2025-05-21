---
uni-module: MBNN
---
# Momentum Backpropagation

Momentum [[Backpropagation]] allows a dynamic change of the learning rate in a [[Neural Network]] by including a memory term in the weight update. This will lead to larger steps in the direction of similar [[Gradient|Gradients]] and smaller steps in oscillating or zigzagging gradients. 
$$\Delta w_k=-\eta\left(g_k+\alpha^1 g_{k-1}+\alpha^2 g_{k-2}+\alpha^3 g_{k-3}+\ldots\right)$$
The discounting factor $\alpha$ should be between zero and one. 

Via the [[Geometric Series]] we get for similar [[Gradient|Gradients]]
$$\Delta w=-\frac{\eta}{1-\alpha} g$$
a way to speed up the steps.

And for oscillating gradients ($(-1)^kg$) we get
$$\Delta w=-\frac{\eta}{1+\alpha} g$$
a way to slow down the steps. 

This method is especially helpful when we have flat regions in the parameters of the network. 

It is used in the [[Adam]] optimizer.