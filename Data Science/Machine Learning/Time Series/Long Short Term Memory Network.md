---
aliases:
  - LSTM
  - LSTMs
uni-module: MBNN
---
# Long Short Term Memory Network

A special form of [[Recurrent Neural Network]] that works well with long-range dependencies in the sequences. It also reduces the risk of vanishing or exploding [[Gradient|Gradients]]. 

**Intuition**
It adds longer lasting memory to a [[Recurrent Neural Network]]. 

$$s_t=\operatorname{switch}_1\left(u_t\right) \cdot s_{t-1}+\text { switch }_2\left(u_t\right) \cdot \tanh \left(A s_{t-1}+B u_t\right)$$

A more efficient way by an [[Exponential Smoothing]] embedding.
$$s_t=(1-D) s_{t-1}+D \tanh \left(A s_{t-1}+B u_t\right)=s_{t-1}+D\left(\tanh \left(A s_{t-1}+B u_t\right)-s_{t-1}\right)$$
![[Bildschirm­foto 2023-04-11 um 23.32.46.png]]

The matrix $D$ can be learned by the model. It can thus decide on its own how much long term memory it needs.

## Feature Selection

[[Feature Selection]] using [[Sensitivity Analysis]]

## Resources

http://colah.github.io/posts/2015-08-Understanding-LSTMs/
