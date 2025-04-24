---
uni-module: "KDD"
---

# Mahalanobis Distance

Measures distance between an object $x$ and the [[Wahrscheinlichkeitsmaß|Distribution]] of the dataset.
$$\operatorname{MD}(\mathbf{x})=\sqrt{(\mathbf{x}-\overline{\mathbf{x}})^T \mathbf{C}^{-1}(\mathbf{x}-\overline{\mathbf{x}})}$$
with $\overline{x}$ [[Arithmetic Mean]] and $C$ the [[Kovarianz|Covariance]] matrix.

Use [[Grubbs Test]] on this measure to detect outliers.
