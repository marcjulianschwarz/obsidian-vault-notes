---
uni-module: AI
aliases:
  - embedded
---
w# Word Embedding

A Word Embedding is a mapping from words in context into a real valued vector space $\mathbb{R}^n$ used for [[Nichtlineares Optimierungsproblem|NLP]].

Also see [[One-Hot-Encoding]].

Uses the [[Tokenization]] of the text.

- [[TF-IDF]]

- [[POS Tagging]] example 

- [[Recurrent Neural Network]]
- [[Bidirectional Recurrent Neural Network]]
- [[Long Short Term Memory Network|LSTMs]] can better learn grammatical dependencies 

## Semantic Word Embedding 

Word embeddings that take context into account by placing vectors in the vectorspace in such a way that they show relations among words. That way you can even encode word relations through vector differences

- Word2vec 
	- Trained with [[Common Bag Of Words]]
- GloVe
- fastText (multilingual)



