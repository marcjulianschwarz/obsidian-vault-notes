---
uni-module: AI
---
# Conditional Independence

The [[Zufallsvariable|Random Variable]] $Z_1$ is conditionally independent of $Z_2$ given $Z$ if 
$$P\left(Z_1, Z_2 \mid Z\right)=P\left(Z_1 \mid Z\right) \cdot P\left(Z_2 \mid Z\right)$$

and we get 
$$P\left(Z_1 \mid Z_2, Z\right)=P\left(Z_1 \mid Z\right)$$
So we can drop parts of the right side when we have conditional independence. This is heavily exploited in [[Bayesian Network|Bayesian Networks]].


- [[Bayes Formel|Bayes Rule]] with multiple evidence 
- dimensionaloty reducion
- drop probabilities that we alread know via causal things in the world 
- clever ordering can make computations more efficient 
- seen quite often, Independence not so much 
