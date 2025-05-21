---
uni-module: AI
---
# Perplexity

An [[Intrinsic Evaluation]] method that answers:

> How uncertain is a model about the predictions it makes? Confident models often correlate with accurate models. 

[[Surprisal]] → [[Expected Information|Entropy]] → [[Perplexity]]

$$\operatorname{PP}(p)=2^{\operatorname{Entropy}(p)}=2^{-\sum_ip_i\operatorname{log}_2(p_i)}$$
The model is *"as confused"* as if it had to randomly choose between $\operatorname{PP}(p)$ different units. This also means that the wors-case scenario is fixed by the [[Branching Factor]].


**Ressources**
- [How Good is Your Chatbot? An Introduction to Perplexity in NLP](https://www.surgehq.ai/blog/how-good-is-your-chatbot-an-introduction-to-perplexity-in-nlp)


## Artificial Intelligence 2 

The perplexity of a sequence $\mathrm{C}_{1: N}$ is 
$$\text { Perplexity }\left(\mathrm{c}_{1: N}\right):=P\left(\mathrm{c}_{1: N}\right)^{-\left(\frac{1}{N}\right)}$$

**Intuition**
The reciprocal (Kehrwert) of probability, normalized by sequence length.


For a language with n characters or words and a language model that predicts that all are equally likely, the perplexity of any sequence is n. If some characters or words are more likely than others, and the model reflects that, then the perplexity of correct sequences will be less than n.

