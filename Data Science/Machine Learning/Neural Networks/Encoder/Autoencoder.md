---
uni-module: MBNN
---
# Autoencoder

Has an [[Encoder-Decoder-Architecture]]. We can use it to get rid of redundant information and compress the rest of the information in a nearly lossless way such that we can always reconstruct the original data from the compressed/auto-encoded data. 

![[Bildschirm­foto 2023-06-08 um 13.12.26.png]]

so here, we either learn matrices $A$ and $B$ or $A$ and $A^T$.
This is in parts similar to [[Principle Component Analysis|PCA]].

It can e.g. be used for [[Anomaly Detection]].

## Encoder 

A module that [[Data Compression|compresses]] the input data into an *encoded representation* that is way smaller than the input data ([[Dimensionality Reduction]]).

## Bottleneck 

A module that contains the compressed data.

## Decoder 

A module that can decompress the compressed data and reconstructs the original data.


## Linear Auto-Encoder 




## Types of Autoencoders 

There are five popular types of autoencoders:
- [[Undercomplete Autoencoder]] 
- [[Sparse Autoencoder]]
- Contractive Autoencoder 
- Denoising Autoencoder 
- [[Variational Autoencoder]]

