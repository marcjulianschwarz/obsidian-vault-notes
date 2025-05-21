---
uni-module: "KDD"
---
# Wavelet Transform

Decompose a signal into different frequency subbands which preserve relative distances and make natural clusters visible.
→ Can be used in [[Image Compression]].

## Discrete Wavelet Transform

Transform vector into a different vector with wavelet coefficients.

Result → Compressed Approximation → only store strongest wavelet coefficients.

### Algorithm

_Input:_ Initial vector $X=(x_1,...,x_n)$

One Iteration:
Build pairs: $(x_1, x_2), (x_2, x_3), ..., (x_{n-1}, x_n)$

For each pair:

- smooth pair (average)
- calculate difference $p_1-x$
  Create new vector with smoothed v3alues and store the differences.

Resulting vector includes the last smoothed values and all differences.

Replace small coefficients with zero to compress while retaining significant coefficients.

## Advantages

- efficient, linear complexity
- multi-resolution → detct arbitrary shaped clusters at different scales
- removes [[Outlier]], insensitive to noise and input order
- Hat-shaped filters → removes weaker information at boundaries of clusters
