---
uni-module: "ISSP"
---

# Runs test for long 01-sequence

To determine whether a 01-sequence is random or not, we develop a test based on [[Zentraler Grenzwertsatz|Normalapproximation]].
We know by e.g. simulation that the number of runs in a 01-sequence is approximately normally distributed. We can thus create a [[Confidence Interval]] for which in 95% of the experiments the number of runs will lie in.

We calculate

$$
\mu=1+\frac{2 n_{0} n_{1}}{n}, \quad \sigma^{2}=\frac{(\mu-1)(\mu-2)}{n-1}
$$

where $n_{0}$ equals the number of zeroes and $n_{1}$ the number of ones.

You can approximate the interval boundaries if $n_0=n_1\geq 20$ with:
$$\mu =n/2$$
$$2\sigma=\sqrt{n}$$

Number of runs is normally distributed with the above parameters. Thus [[Acceptance Domain]] is defined below.

## Test decision:

Accecpt randomness hypothesis if number of runs (concecutive runs of 1s or 0s) is in $$
[\mu-2 \sigma, \mu+2 \sigma]

$$
In only about 5% of all cases the hypothesis will be rejected although it is true (Type 1 Error).

However in a lot of cases the hypothesis will be accepted even though it is false (Type 2 Error).

One can show this fact like this:
$$\mathbb{P}(R \in[\mu-2 \sigma, \mu+2 \sigma])=\mathbb{P}(-2 \leq(R-\mu) / \sigma \leq 2) \rightarrow \Phi(2)-\Phi(-2) \approx 0.954$$
Thus in 95% of all cases the hypothesis will be accepted.


$$
