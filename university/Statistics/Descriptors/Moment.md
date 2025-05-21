---
uni-module: "ISSP"
---

# Moment

$$m_n^p:=\frac{1}{n} \sum_{i=1}^n x_i^p$$

- $p=1$ [[Arithmetic Mean]]
- $p=-1$ harmonic mean

The [[Erwartungswert|Expectation]] $E_F(X^p)$ is then called the $p^{th}$ moment of $F$.

We have

$$
\frac{1}{n} \sum_{i=1}^n x_i^r \longrightarrow \mathbb{E}_F\left(X^r\right)
$$

hence the moment can be used to estimate the [[Erwartungswert|Expectation]] of an [[Empirical cumulative distribution functions|ECDF]].

We also get a 95% [[Confidence Interval]]

$$
\left|m_n^p-\mathbb{E}_F\left(X^p\right)\right| \leq \frac{2 \sqrt{\mathbb{V}_F\left(X^p\right)}}{\sqrt{n}}
$$
