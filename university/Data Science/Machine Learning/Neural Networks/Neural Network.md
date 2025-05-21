---
tags: note, datascience, keep
alias: ["NN", "Neural Networks", "NNs"]
---
# Neural Network

Basic Neural Network architecture

![[CleanShot 2023-11-17 at 17.49.25@2x.png]]

- Weights 
- Bias Weight 
	- needed to allow for general hyperplanes that do not necessarily go through the origin 
	- in [[Recurrent Neural Network|RNNs]] a missing bias weight can be corrected by one of the internal state neurons.
- [[Activation Function]]
- [[Backpropagation]]
- 

A neural network can always be expanded by the concatenation of mutliple layers in contrast to [[Taylor-Approximation|Taylor Expansion]] where complexity is increased with additive terms.

[[Universal Approximation Theorem]]


**Existence Theorem**
3-layer neural nets can approximate any [[Stetigkeit|continous]] function on a [[Kompaktheit|compact]] domain.

> [!QUestion]- Why do we need a compact input domain?
> We can only use a *finite* number of non-linear functions to model a *finite* diameter of the input domain.
> Open sets can create singularities at the boundary which can not be modelled by non-linear functions.


For example:
- [[Feed-forward Neural Network]]
- [[Deep Neural Network]]

## Specialized Networks 

- [[Recurrent Neural Network]]
  - [[Long Short Term Memory Network]]
  - [[Error Correction Neural Network|ECNN]]
  - [[Historical Consistent Neural Network|HCNN]]
