---
uni-module: "KDD"
---

# Binning

Used to discretize continous/numerical data sequences.

## Equal Width (distance)

Dividing the data into equal sized intervals with a width that can be calculated like this:
$$\frac{max-min}{N}$$

- [[Outlier]] can dominate
- Skewed data isn't handled well

## Equal Depth (frequency)

Dividing the data into intervals, each containing approximately the same numper of [[Sample|samples]].

- Scales really good
- Managing [[Categorical Data]] can be hard

_Other Methods_

- [[Histogram Analysis]]
