---
uni-module: AI
aliases:
  - CBOW
tags:
  - Algorithmus
---
# Common Bag Of Words

**Architecture for a single word**

![[CleanShot 2023-10-03 at 21.52.58@2x.png]]

The hidden layer does not have an [[Activation Function]]. The output layer computes the [[Softmax]].

**Architecture for multiple words**

You can interpret the second / middle word vector here as the current word and the first and last word vectors are its context which has influence on the embedding. 

![[CleanShot 2023-10-03 at 21.57.06@2x.png]]