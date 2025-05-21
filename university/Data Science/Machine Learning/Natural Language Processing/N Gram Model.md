---
uni-module: AI
aliases:
  - Trigram Model
---
# N Gram Model

A [[Markov Process]] of order $n-1$.

So for a [[n-Gramm|Bigram]] model we would have a [[Markov-Kette|Markov Chain]] and for a [[n-Gramm|Trigram]] model we would have a [[Markov Process]] of order $2$.

For [[n-Gramm|Trigram]] model:
$$P\left(\mathrm{c}_i \mid \mathrm{c}_{1: i-1}\right)=P\left(\mathrm{c}_i \mid \mathrm{c}_{(i-2)}, \mathrm{c}_{(i-1)}\right)$$
Using the [[Probability Chain Rule|Chain Rule]] and [[Markov Property]] we get for a sequence of characters 
$$P\left(\mathrm{c}_{1: N}\right)=\prod_{i=1}^N P\left(\mathbf{c}_i \mid \mathbf{c}_{1: i-1}\right)=\prod_{i=1}^N P\left(\mathbf{c}_i \mid \mathbf{c}_{(i-2)}, \mathbf{c}_{(i-1)}\right)$$
Thus, a trigram model for a language with 100 characters, P(c,|ci-2:i-1) has
1.000.000 entries. It can be estimated from a corpus with 107 characters.

Can be used for relatively bad [[Natural Language Generation]] or for 
- [[Language Identification]]
- Spelling Correction 
- [[Genre Classification]]
- [[Named Entity Recognition]]