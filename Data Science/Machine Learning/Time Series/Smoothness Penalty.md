---
uni-module: "MBNN"

alias: "Normalized Curvature"
---

# Smoothness Penalty

$$P=\frac{1}{T} \sum_{t=1}^T \frac{\left(\left(x_{t+1}-x_t\right)-\left(x_t-x_{t-1}\right)\right)^2}{\left(x_{t+1}-x_t\right)^2+\left(x_t-x_{t-1}\right)^2}$$

From this we get nice properties such as

- enforced angle smoothness
- enforced constant velocity
- partly enforced noise cancellation
