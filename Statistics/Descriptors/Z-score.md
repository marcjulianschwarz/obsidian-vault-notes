---
uni-module: "KDD"

alias: "Standardization"
---

# Z-score

Used to standardize data.

The Z-score is a simple calculation that answers the question, “Given a data point, _how many [[Standardabweichung|standard deviations]] is it away from the [[Arithmetic Mean|mean]]_?”
Negaitve when the value is below the [[Arithmetic Mean|mean]] and positibe else.
$$z=\frac{x_i-\mu}{\sigma}$$
We then know that the [[Erwartungswert|Expectation]] of $z$ is $0$ and the [[Varianz|Variance]] is $1$. And we know the distribution of $z$ is

$$
F_Z(t)=F_Y(t \sqrt{\mathbb{V}(Y)}+\mathbb{E}(Y))
$$

## Alternaviten:

- [[Mean Absolute Deviation]]
