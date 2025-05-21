---
uni-module: AI
aliases:
  - BOW
---
# Bag Of Words

A multiset of words from a [[Vocabulary]]. 

Can be represented as a [[Word Frequency Vector]] where [[Out Of Vocabulary|OOV]] words are ignored. 

A query and document are similar iff the angle between their [[Word Frequency Vector]] is small. 

[[Euclidean Dot Product Formula]]