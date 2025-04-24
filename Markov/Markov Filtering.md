---
uni-module: AI
aliases:
  - Filtering
---
# Markov Filtering

A type of [[Markov Inference]] for computing the current [[Belief State]] (probability distribution) given previous evidence. 
$$\mathrm{P}\left(\mathrm{X}_t \mid \mathrm{e}_{1: t}\right)$$
We want to find this iteratively (via recursion). So we first define
$$f_{0:k}=P(S_k\mid e_{0:k}).$$
Given the above and using the [[Bayes Formel|Bayes Rule]] with [[Probability Normalization|Normalization]], the **base case** is
$$f_{0:0}=\alpha P(e_0\mid S_0)\cdot P(S_0).$$
Now the **recursive case** is 
$$f_{0:k}=\alpha P(e_k\mid S_k)\sum_{s_{k-1}}{P(S_k\mid s_{k-1})\cdot f_{0:(k-1)}}$$
**Apply**
- Use the base case to directly calculate the first probability distribution, make sure to normalize the values 
- Expand the sum in the recursive case 
- Expand the [[Zufallsvariable|Random Variables]] $S_k$ in the recursive case with angled brackets 
- Then fill in all probabilities
- Calculate and normalize the result 

- [Filtering 1](https://www.youtube.com/playlist?list=PLdBx38JxhMNsihN1q71ouR7KaQ7wV1sal)
- [Filtering 2](https://www.youtube.com/playlist?list=PLdBx38JxhMNtL3J7ieNpUQvc7y3bKYgx-)