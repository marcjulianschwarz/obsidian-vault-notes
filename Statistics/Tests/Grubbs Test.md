---
uni-module: "KDD"

alias: "Maximum Normed Residual Test"
---

# Grubbs Test

[[Null Hypothesis]] and other hypothesis:

$$
\begin{aligned}
H_{0}: \text{No outliers} \\
H_{1}: \text{Exactly one outlier}
\end{aligned}
$$

[[Test Statistic]]

$$G=\frac{\max \left|x_i-\bar{x}\right|}{s}$$
with [[Arithmetic Mean]] $\overline{x}$ and sample [[Standardabweichung|standard deviation]] $s$.

Reject [[Null Hypothesis]] when
$$G>\frac{N-1}{\sqrt{N}} \sqrt{\frac{t^2_{\frac{\alpha}{2 N}, N-2}}{N-2+t^2_{\frac{\alpha}{2 N}, N-2}}}$$
where $t$ is the [[t-Distribution]].
