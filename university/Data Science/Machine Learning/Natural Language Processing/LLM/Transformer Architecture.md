---
uni-module: AI
aliases: []
---
# Transformer Architecture 


[[Transformer Encoder]]

Uses a [[Decoder]] - [[Encoder]] [[Sequence To Sequence Model|seq2seq]] Architecture.


![[Transformer Model Architecture.canvas]]
## Pros compared to other architectures 

- [[Self-Attention]] layers were found to be faster than [[Recurrent Neural Network|RNN]] layers for shorter sequence lengths and can be restricted to consider only a neighborhood in the input sequence for very long sequence lengths. 
- The number of sequential operations required by a [[Recurrent Neural Network|RNN]] layer is based on the sequence length, whereas this number remains constant for a self-attention layer. 
- In [[Convolutional Neural Network|CNNs]], the kernel width directly affects the long-term dependencies that can be established between pairs of input and output positions. Tracking long-term dependencies would require using large kernels or stacks of convolutional layers that could increase the computational cost.
- more parallelizable 
- requiring significantly less time to train 
- 




## Resources 

The Annotated Transformer
https://nlp.seas.harvard.edu/annotated-transformer/

Transformer from Scratch
https://e2eml.school/transformers.html#attention

Transformers from Scratch (2)
https://peterbloem.nl/blog/transformers

The Illustrated Transformer
https://jalammar.github.io/illustrated-transformer/

Attention is all you need (Talk)
https://www.youtube.com/watch?v=rBCqOTEfxvg

Lecture on YT
https://www.youtube.com/playlist?list=PLIXJ-Sacf8u60G1TwcznBmK6rEL3gmZmV

Transformers (StatQuest)
https://www.youtube.com/watch?v=zxQyTK8quyY

Transformers: Zero to Hero
https://www.youtube.com/watch?v=rPFkX5fJdRY

Attention is all you need (Paper)
https://arxiv.org/pdf/1706.03762.pdf

Deconstructing BERT (Visualize the Inner Workings of Attention)
https://towardsdatascience.com/deconstructing-bert-part-2-visualizing-the-inner-workings-of-attention-60a16d86b5c1
