---
uni-module: AI
---
# Kernel Trick

In [[Linear Regression]] we used a basis function to predict polynomial functions. We can do the same with SVMs. We apply our basis function to both the training data point and the data point that we want to do predictions on.

The basis function will be calculated a lot of times because we have $n^2$ summands for the optimization and $n$ for the final prediction.

However, from [[Karush-Kuhn-Tucker Conditions]] we know that $\alpha _i$ will be zero for most of the times (only when it is a [[Support Vector]], it is non-zero). This means, we dont even need to calculate the basis function all the time. To make use of this [[Sparsity]] and therefore simplifying the computations we use the Kernel Trick. Instead of explicitly computing the basis function, the Kernel function uses implicit calulations.

There are different kinds of Kernel Functions:

### Linear Kernel

- only useful if the data is linearly seperable

- [[Radial Basis Function Kernel]]

### Polynomial Kernel
