---
uni-module: "XAI"

alias: "Gradient-weighted Class Activation Mapping"
---

# Grad-CAM

$$A_{ij}^k$$

Average over all [[Gradient|gradients]] for class $c$ and
$$\alpha_k^c=\frac{1}{Z} \sum_i \sum_j \quad \frac{\delta y^c}{\delta A_{i j}^k}$$
