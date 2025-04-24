---
uni-module: AI
---
# Language Identification

Given a text, determine the [[Natural Language]] it is written in. 

## Method 

Build a [[N Gram Model|Trigram Model]] 
$$\mathrm{P}\left(\mathrm{c}_i \mid \mathrm{c}_{i-2: i-1}, \ell\right)$$
for every language $\ell$.

Apply [[Bayes Formel|Bayes Rule]] and the [[Markov Property]] to get the most likely language 

$$\begin{aligned}
\ell^* & =\underset{\ell}{\operatorname{argmax}}\left(P\left(\ell \mid \mathbf{c}_{1: N}\right)\right) \\
& =\underset{\ell}{\operatorname{argmax}}\left(P(\ell) \cdot P\left(\mathbf{c}_{1: N} \mid \ell\right)\right) \\
& =\underset{\ell}{\operatorname{argmax}}\left(P(\ell) \cdot \prod_{i=1}^N P\left(\mathbf{c}_{\boldsymbol{i}} \mid \mathbf{c}_{\boldsymbol{i}-2: i-1}, \ell\right)\right)
\end{aligned}$$
The [[Prior Probability]] of the language is not a critical factor.

**Intuition**
When $l$ is not the correct language all probabilities of character sequences $c_{i-2:i}$ will be low. For the correct language they will be a lot higher.

