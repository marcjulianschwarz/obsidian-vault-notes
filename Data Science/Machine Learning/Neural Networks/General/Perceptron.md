# Perceptron

The perceptron is a model of a human [[Nervenzelle|Neuron]]. 

$$y=a(w\cdot x +b)$$

**Intuition**
It has multiple inputs $x$. Each input will be multiplied by a weight $w$. This lets the model control how relevant information from different inputs is. 

Then all weighted inputs will be summed up and a bias value $b$ will be added on top (the bias is like the resting potential of a human neuron). And finally, an [[Activation Function]] $\sigma$ (usually [[Logistic Function|Sigmoid Function]]) determins whether the neuron triggers and sends the value to the output.

The perceptron is not recommended to be used in practice as it does not converge for nonlinear decision boundaries.

## Training Loop 
![[percep8.png]]

Also see [Implementing a Simple Perceptron for Binary Classification - Marc's Notes](https://www.marc-julian.de/posts/2023/6/Implementing%20a%20Simple%20Perceptron.html) for some code.

A similar model is the so called [[Adaptive Linear Unit]].

## Learning Rule 

$$w_i \longleftarrow w_i+\alpha \cdot\left(y-h_w(x)\right) \cdot x_i$$

where $\alpha$ is the learning rate. 
