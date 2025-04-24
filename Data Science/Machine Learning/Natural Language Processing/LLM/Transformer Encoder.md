# Transformer Encoder

An [[Encoder]] that takes the [[Word Embedding|embedded]] text as input and applies [[Multi-Head Attention]] to it on a stack of $N=6$ identical layers. The output of it is then fed into the [[Transformer Decoder]].

Each layer has two sublayers 
- [[Multi-Head Attention]]
- [[Feed-forward Neural Network]]

Each of the sublayers has a [[Residual Connection]] that lets information go past each layer. They are then added onto the output of the normalized sublayers. 
$$\operatorname{LayerNorm}(x+\operatorname{Sublayer(x)})$$
All sublayers as well as the [[Word Embedding]] layers produce outputs of dimension $d_{\text{model}}=512$.

