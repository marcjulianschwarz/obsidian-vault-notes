---
uni-module: AI
aliases:
  - seq2seq
---
# Sequence To Sequence Model

Uses two coupled [[Recurrent Neural Network|RNNs]] in the form of an [[Encoder]] and [[Decoder]].

**Intuition**
The encoder serves as some kind of *memory* that the decoder can rely on. 

![[CleanShot 2023-10-03 at 22.11.30@2x.png]]

Example setup with [[Long Short Term Memory Network|LSTMs]] for translation.

![[CleanShot 2023-10-03 at 22.11.43@2x.png]]