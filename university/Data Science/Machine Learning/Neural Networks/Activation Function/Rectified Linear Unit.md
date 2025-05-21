---
alias:
  - RELU
---
# Rectified Linear Unit

An [[Activation Function]], mainly used in Image Recognition. 

$$f(x)=\left\{\begin{array}{lll}
x & & x \geq 0 \\
& \text { if } & \\
0 & & x<0
\end{array}\right\}$$

## Smoothed

$$f(x)=\frac{1}{p} \ln \left(1+e^{p x}\right)$$
with [[Logistic Function]] as [[Gradient]]
$$f^{\prime}(x)=\frac{1}{1+e^{-p x}}.$$



**Pros**
- does not squeeze error flow in backward pass
- can completely block error flow when values are negative in backward pass (helpful for image recognition?)


**Cons**
- exploding values in forward pass 
- not differentiable at zero 
- does not squeeze error flow in backward pass





