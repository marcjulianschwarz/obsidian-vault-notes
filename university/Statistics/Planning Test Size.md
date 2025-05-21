---
uni-module: "ISSP"
---

# Planning Test Size

We would like to minimize [[Type 2 Error]] to hold to our Hypothesis. We thus would like to know how many samples we should take to get below a certain threshold.

## One-Sided Tests

For [[One-Sided Gauß Test]]

$$\beta(\mu)=\Phi\left(z_{1-\alpha}-\frac{\left|\mu-\mu_0\right|}{\sigma / \sqrt{n}}\right)$$

Thus by applying the inverse we get:
$$n \geq n_0:=\frac{\left(z_1-\alpha-z_\beta\right)^2 \sigma^2}{\left|\mu-\mu_0\right|^2}$$

## Two-Sided Test

For [[Two-Sided Gauß Test]]

$$\beta(\mu)=\Phi\left(z_{1-\alpha / 2}-\frac{\left|\mu-\mu_0\right|}{\sigma / \sqrt{n}}\right)+\Phi\left(z_{1-\alpha / 2}+\frac{\left|\mu-\mu_0\right|}{\sigma / \sqrt{n}}\right)-1$$

Here we have to solve for $n_0$ numerically. For example by plotting and reading the value.
