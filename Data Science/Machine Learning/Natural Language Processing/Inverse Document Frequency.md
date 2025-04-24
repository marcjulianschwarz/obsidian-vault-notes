---
uni-module: AI
aliases:
  - idf
  - IDF
---
# Inverse Document Frequency

Similar to the normalized [[Term Frequency]] we want to find out how much a given word $t$ is found in a collection of documents $D$. 

$$\operatorname{idf}(t, D):=\log _{10}\left(\frac{N}{|\{d \in D \mid t \in d\}|}\right)$$

**Intuition**
This formula is near $0$ when a word is present in nearly all documents. For example, the word *"the"* will most likely have a value of zero. This will ensure that "meaningless" words will not be used for [[Information Retrieval]].
