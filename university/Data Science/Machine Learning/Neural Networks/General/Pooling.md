---
uni-module: ML4ENG
---

# Pooling

Deep in the network after multiple [[Convolution]] layers the number of features quickly grows. To reduce the amount of features we can summarize them with a Pooling Operation.

It works like this:
![[IMG - Pooling.png]]

Notice that the stride is usually bigger than with [[Convolution]].

The example above shows one possible pooling function. But there are other commonly used functions:

- Maximum
- Average
- $L^2$ - [[Norm]] → all values squared and summed up.

Combining [[Convolution]] and Pooling can lead to a network looking like this:
![[IMG - Convolution and Pooling layers.png]]
