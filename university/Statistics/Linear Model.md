---
uni-module: "ISSP"
---

# Linear model

A linear model consists of a matrix $A$ which contains all coefficients. We can then write our set of possible _regression functions_ like this:

$$f_{\gamma}(t) =A\cdot\gamma$$

Of course there are also other models which can include non-linearities like:

- [[Exponential Growth]]
- [[Allometric Growth]]

## Simple linear model

This is how a simple two dimensional linear model can look like:
$$f(x) = w_0 \cdot x_0 + w_1 \cdot x_1 = y$$

The input is the x vector with $x_0$ and $x_1$ as values. The same applies to the weights.
Finding the best weights to describe $y$ with our function is called _Fitting_.

Usually a residual error $\epsilon$ is part of the equation. A lot of times it has a Gaussian distribution.

In vector notation the general linear model looks like this:
$$f(x) = w^Tx + \epsilon = y$$

Now we have to optimize the model parameters:
