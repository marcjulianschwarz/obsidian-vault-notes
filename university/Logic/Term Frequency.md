---
uni-module: AI
aliases:
  - Raw Term Frequency
  - TF
---
# Term Frequency

The number of occurrences of a word $w$ in a document $d$. 

The **normalized** term frequency is divided by the size of the document $d$.
$$\operatorname{tf}(w, d)=\frac{n}{\mid d\mid}$$
where $n$ is the number of occurrences of $w$ in $d$.

They are induced by adding up [[One-Hot-Encoding|one hot]] [[Embedding|Word Embeddings]], see [[TF-IDF Word Embedding]]

Also see [[Inverse Document Frequency]].