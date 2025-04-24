---
uni-module: "MBNN"
---
# Hidden Layer

A layer that is not the output and not the input layer. 

## Estimate its size 

With the [[Korrelation|Pearson Correlation]] we can see when two [[Nervenzelle|Neurons]] are doing the same job.

$$\left\langle f_i, f_j\right\rangle=\frac{\sum_t\left(f_i(t)-\bar{f}_i\right)\left(f_j(t)-\bar{f}_j\right)}{\sqrt{\sum_t\left(f_i(t)-\bar{f}_i\right)^2 \sum_t\left(f_j(t)-\bar{f}_j\right)^2}}$$
When the highest [[Korrelation|Correlation]] is near one we have to reduce the size. Otherwise we can increase it. 

