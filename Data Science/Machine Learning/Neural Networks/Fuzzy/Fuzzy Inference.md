---
uni-module: MBNN
---
# Fuzzy Inference

A rule $b_k$ is a product (AND) of several [[Membership Function|Membership Functions]] $mf_j$ that can be active or not via the learnable parameter $p_{kj}$.
$$b_k(x)=\prod_{j=1}^M\left(m f_j(x)\right)^{p_{k j}}=\exp \left(\sum_{j=1}^M p_{k j} \ln \left(m f_j(x)\right)\right)$$
The rewritten logarithmic form can be expressed as a [[Neural Network]].