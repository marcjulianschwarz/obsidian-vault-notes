---
uni-module: "KDD"

alias: "MAD"
---

# Mean Absolute Deviation

$$
\operatorname{MAD}\left(X=\left\{x_{1}, x_{2}, \ldots, x_{n}\right\}\right)=\frac{1}{n} \sum_{i=1}^{n}\left|x_{i}-\bar{x}\right|
$$

where $$\bar{x}=\frac{1}{n} \sum_{i=1}^{n} x_{i}$$, thus $$z_{i}=\frac{x_{i}-\bar{x}}{\sqrt{\frac{1}{n} \sum_{i=1}^{n}\left(x_{i}-\bar{x}\right)^{2}}}$$

## Median Absolut Deviation

Robust against [[Outlier|Outliers]].
