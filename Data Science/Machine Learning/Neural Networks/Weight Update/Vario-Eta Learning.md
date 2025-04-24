---
uni-module: MBNN
---
# Vario-Eta Learning

The update rule is 
$$\Delta w_t^i=-\frac{1}{\sqrt{\frac{1}{T} \sum\left(g_t^i-g^i\right)^2}} g_t^i$$

The sum is computed using [[Exponential Smoothing]].

