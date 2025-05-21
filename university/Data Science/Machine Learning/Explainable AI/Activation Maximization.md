---
uni-module: "XAI"
---

# Activation Maximization

> Finding the input that maximizes the activation of a [[Unit]], mostly used to visualize the feature detectors in a [[Convolutional Neural Network|CNN]].

For a single neuron we can write an optimization problem like this
$$i m g^*=\arg \max _{i m g} h_{n, x, y, z}(i m g)$$
where

- $h$ is the [[Activation Function]]
- $x,y$ encode the position of the [[Unit]]
- $n$ is the layer
- $z$ is the channel index

The mean activation for an entire channel can be achieved by averaging over all neruons in that channel
$$i m g^*=\arg \max _{i m g} \sum_{x, y} h_{n, x, y, z}(i m g)$$
![[Bildschirmfoto 2023-07-23 um 19.32.29.png]]

Using the minimum instead of the maximum is not working. It will correspond to ...

You can start with an image from

- the training [[Dataset|data]]
- random noise
  - need to do [[Regularisation]] like
    - jittering
    - rotation
      - linear combination of all channels leads to entangled features (makes interpretability harder)
    - scaling
    - frequency penalization to reduce variance of neighboring pixels
    - GANs
    - denoising [[Autoencoder]]
