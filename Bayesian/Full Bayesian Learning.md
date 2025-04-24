---
uni-module: AI
aliases:
  - Bayesian Learning
---
# Full Bayesian Learning

**Intuition** 
Bayesian updating of a probability distribution over the [[Hypothesis Space]].

- $H$ is a [[Zufallsvariable|Random Variable]] with hypothesis values $h_1,h_2,\dots$ with [[Prior Probability]] $P(H)$
- $D_j$ is a random variable for which $d_j$ is a possible outcome 
- $d=d_1,\dots,d_N$ is the training [[Dataset]] of an [[Inductive Learning]] problem 

Given the data we could calculate for each hypothesis $h_i$ its [[Posterior Probability]] with [[Bayes Formel|Bayes Rule]] und [[Probability Normalization|Normalization]]
$$P\left(h_i \mid d\right)=\alpha \cdot P\left(d \mid h_i\right) \cdot P\left(h_i\right)$$
where we call $P(d\mid h_i)$ the [[Likelihood]] of the data under the hypothesis and $P(h_i)$ the hypothesis [[Prior Probability|Prior]].

## Prediction 

$$
\mathrm{P}(X \mid d)=\sum_i \mathrm{P}(X \mid d, h_i) \cdot P(h_i \mid d)=\sum_i \mathrm{P}(X \mid h_i) \cdot P(h_i \mid d)
$$

**Problem**
We are summing over the entire [[Hypothesis Space]] by looking at all $h_i$. This is of course intractable for most large spaces. 

**Solution**
We try to approximate the above probability by getting rid of the sum over the entire [[Hypothesis Space]]. Instead we only look at the most probable hypothesis. 

- [[Maximum A Posteriori Learning]]
- an alternative representation [[Minimum Description Length Learning]]
- [[Maximum Likelihood Estimation]]
