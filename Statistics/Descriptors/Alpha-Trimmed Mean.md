---
uni-module: "ISSP"
---

# Alpha-Trimmed Mean

An alternative to [[Arithmetic Mean]] which is more robust against [[Outlier]] where the lower and upper $\alpha$ percent are being truncated.
$$\alpha\in[0,1/2)$$ $$k=\lfloor n\alpha \rfloor$$$$\bar{x} = \frac{1}{n-2k}(x_{k+1} + ... + x_{n-k})$$

- Order data
- discard lowest and highest $\alpha$ percent
- Compute [[Arithmetic Mean]] on remaining data
- 50% trimmed mean corresponds to [[Median]]
