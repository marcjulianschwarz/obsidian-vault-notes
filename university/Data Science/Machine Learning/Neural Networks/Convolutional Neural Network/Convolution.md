---
uni-module: ML4ENG
---
# Convolution

As mentioned before, a human brain has specialized regions. Our visual cortex is responsible of processing visual information from our eyes.

If we compare our [[Multilayer Perceptron]] with a Cortical Neuron (responsible to process information fromt the retinas), we can see a big difference. The [[Perceptron]] has all neurons of the previous layer connected to all new neuros where the cortical neuron only has a few neurons from the previous layer connected. → Model this behaviour.

## The Convolution Operation

Using the following formula, our output now only depends on a smaller subset of our inputs.

![[IMG - Convolution.png]]

Of course we can apply this operation on multiple layers → [[Convolutional Neural Network]] (CNN).

## Maths

- Input: x times y
- Kernel size: k times c
- Output: x - k + 1 times y - c + 1

→ Capturing the spatial dependencies in images
