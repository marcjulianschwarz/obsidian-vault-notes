---
uni-module: AI
aliases:
  - Maximum A Posteriori Approximation
  - MAP
  - MAP Learning
---
# Maximum A Posteriori Learning

Instead of [[Full Bayesian Learning]] we try to choos the MAP hypothesis $h_{\text{MAP}}$ that maximizes 
$$P(h_i\mid d).$$
This can be rewritten using [[Bayes Formel|Bayes Rule]] to 
$$P(d\mid h_i)\cdot P(h_i)$$
(we can leave out $P(d)$ as it is constant for all hypothesis. We could in theory even leave out $P(h_i)$ when the dataset is large → [[Maximum Likelihood Estimation|ML Learning]]).

or even better by utilizing the properties of the logarithm 
$$\log _2\left(P\left(\mathrm{~d} \mid h_i\right)\right)+\log _2\left(P\left(h_i\right)\right).$$
So we get $h_{\text{MAP}}$ with 
$$\underset{h_i}{\arg\max}\quad \log _2\left(P\left(\mathrm{~d} \mid h_i\right)\right)+\log _2\left(P\left(h_i\right)\right)$$
which requires solving an optimization problem instead.

**Predictions**
The predictions made this way are approximately Bayesian to the extent that 
$$
\mathrm{P}(X \mid d) \approx \mathrm{P}(X \mid h_
{\mathrm{MAP}})
$$
This means, for predictions we have to only compute this one probability and do not have to sum over all possible hypothesis. 

