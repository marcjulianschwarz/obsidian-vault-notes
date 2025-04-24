---
uni-module: KDD
aliases:
  - Naive Bayes Model
  - Naive Bayes
---
# Naive Bayes Classifier

A simpler [[Bayesian Classifier]] which assumes [[stochastisch unabhängig|independent]] attributes / classes which is why we can write 
$$\mathrm{P}\left(\text { c }\mid \text { e }_1, \ldots, \text { e }_n\right)=\alpha\left\langle\text { e }_1, \ldots, \text { e }_n\right\rangle \cdot \mathrm{P}(\text { c }) \cdot \prod_i \mathrm{P}\left(\text { e }_{\boldsymbol{i}} \mid \text { c }\right)$$
Assuming boolean variables (which we can always achieve via [[Binning]] and [[One-Hot-Encoding]]), we have the following parameters in the CPTs 
$$\theta=P(c=\mathrm{T}), \theta_{i 1}=P\left(X_i=\mathrm{T} \mid C=\mathrm{T}\right), \text { and } \theta_{i 2}=P\left(X_i=\mathrm{T} \mid C=\mathrm{F}\right)$$

We can then do a prediction with 
$$\mathrm{P}\left(C \mid x_1, \ldots, x_n\right)=\alpha \cdot \mathrm{P}(C) \cdot \prod_i \mathrm{P}\left(x_i \mid C\right)$$
The cool thing is, that there are only $2n+1$ parameters and there is no search required. Naive Bayes models perform great, even when the data is noisy.

## Calculation of Probabilities

If attribute is [[Categorical Data|categorical]]:
$$P(x_{k}|C_{i})$$
is the number of tuples in class $C_{i}$ having value $x_{k}$ divided by the number of tuples of the class $C_{i}$.

If attribute is [[Stetigkeit|continous]]:
Usually computed based on [[Normalverteilung|Normal Distribution]] with
$$P(x_{k}|C_{i})=G(x_{k},\mu_{C_{i}},\sigma_{C_{i}})$$

> [!Check]+ Pros
>
> - easy to implement
> - but still good results

> [!Warning]+ Cons
>
> - assumption leads to loss of [[Accuracy]]
> - as there will always be some kind of dependency amongst variables
>   - → [[Bayesian Belief Network]]

## Implementation

Use this function to test whether datapoint is more likely for class 1 vs. class 0 by estimating loc and scale from the data for the respective classes.

```python
scipy.stats.norm.pdf(value, loc, scale)
```
