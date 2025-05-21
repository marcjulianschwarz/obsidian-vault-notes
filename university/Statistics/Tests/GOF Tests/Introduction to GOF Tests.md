# Introduction to GOF Tests

All of these tests can only detect deviations from [[Verteilungsfunktion|CDF]] $F$. This means when accepting the [[Null Hypothesis]], there is quite a large [[Type 2 Error]]. The data could for example come from a distribution that is really similar to a normal distribution.

We can do tests for a particular distribution with the [[qq GOF Test for Particular Distribution]].
However sometimes we only want to know whether the datas random mechanism belongs to some class of distributions (for example whether it is normally distributed). In this case we can use the [[qq GOF Test for Class of Distributions]].

In discrete cases we can use the [[Chi-Squared GOF Test for finitely many values]].

This can also be applied when

- [[Class Condition]] is not met
- infinitely many values are present
- continous distribution is used

by grouping ([[Binning]]) the values:
$$l_1=\left(-\infty, a_1\right], l_2=\left(a_1, a_2\right], \ldots, I_s=\left(a_{s-1}, \infty\right) \quad\left(a_1<a_2<\ldots<a_{s-1}\right)$$
For large $n$ one can calculate the relative interval frequency which will coincide with $p_j$. Then use GOF test above.