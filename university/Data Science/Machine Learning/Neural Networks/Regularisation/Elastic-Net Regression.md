---
uni-module: "XAI"
---

# Elastic-Net Regression

Used when there are a _lot_ of features where we dont know whether they are useful or not, so we can't decide between [[Lasso Regression]] and [[Ridge Regression]]. That's why one should use Elastic-Net [[Regression]] in this case.

It combines the strengths of both approaches by including a [[Regularisation]] term for both [[Lasso Regression]] and [[Ridge Regression]].

So we have
$$\lambda_1\mid s\mid +\lambda_2 s^2$$
We can use simple [[K-Fold Cross Validation]] to calculate the best lambdas.

## Resources

- https://www.youtube.com/watch?v=1dKRdX9bfIo
