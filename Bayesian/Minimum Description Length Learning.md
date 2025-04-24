---
uni-module: AI
aliases:
  - MDL Learning
---
# Minimum Description Length Learning

MDL Learning is basically another interpretation for [[Maximum A Posteriori Learning|MAP Learning]] where we interpret the log terms 
$$\log _2\left(P\left(d \mid h_i\right)\right)+\log _2\left(P\left(h_i\right)\right)$$
similar to how we did with [[Information Gain]] in [[Decision Tree Induction]], as the number of bits to encode data given the hypothesis 
$$
-\log _2\left(P\left(d \mid h_i\right)\right)
$$
and the additional bits to encode the hypothesis 
$$-\log _2\left(P\left(h_i\right)\right).$$
So to get the best hypothesis $h_{\text{MDL}}$ we have to minimize the [[Expected Information|Entropy]] of the hypothesis [[Likelihood]].
$$\underset{h_i}{\arg\min}\quad -\log _2\left(P\left(d \mid h_i\right)\right)$$

**Intuition**
If the hypothesis predicts the data exactly, then $P(d\mid h_i)=1$ which yields $\log_2(1)=0$ bits. So this is the preferred hypothesis. 

