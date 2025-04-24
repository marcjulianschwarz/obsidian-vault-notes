---
uni-module: "KDD"

alias: "KDE"
---

# Kernel Density Estimation

Similar to [[Histogram]] but it estimates a continous [[Wahrscheinlichkeitsdichte|PDF]].

It is defined as
$$\hat{f}_h(x)=\frac{1}{n} \sum_{i=1}^n K_h\left(x-x_i\right)=\frac{1}{n h} \sum_{i=1}^n K\left(\frac{x-x_i}{h}\right)$$
with $h$ smoothing parameter, and $K$ the kernel function, in most cases [[Standardnormalverteilung|Standard Normal Distribution]] and
$$K_h(x)=\frac{1}{h} K\left(\frac{x}{h}\right)$$
the scaled kernel.

Make sure to play around with the smoothness parameter to see what works best as it might wash out the data too much if it was chosen too big.

Can be used to spot [[Outlier|Outliers]] the same way it would work with a [[Histogram]].

## Simple Python Implementation

```python
def kde(x, data, h):
    s = 0
    for xx in data:
        s += normpdf((x-xx)/h, 0, 1)
    return 1/(len(data)*h)*s
```
