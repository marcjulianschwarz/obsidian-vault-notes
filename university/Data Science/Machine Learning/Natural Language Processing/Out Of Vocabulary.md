---
uni-module: AI
aliases:
  - OOV
---
# Out Of Vocabulary

Words that are unknown. They appear in the test [[Corpus]] but not training [[Corpus]].

Usually words such as names and locations.

Idea: Model OOV words by
1. adding a new word token, e.g. <UNK> to the [[Vocabulary]],
2. in the training corpus, replacing the respective first occurrence of a previously
unknown word by <UNK>,
3. counting n grams as usual, treating <UNK> as a regular word.
This trick can be refined if we have a word classifier, then use a new token per class, e.g. <EMAIL> or <NUM>.

