---
uni-module: AI
---
# Markov Property

*States do not depend on evidence.*

$X_t$ only depends on $X_{0:t-1}$ and not on the evidence variables $E_{1:t}$.

Other special cases:

**First-order Markov Property:**
$$\mathrm{P}\left(\mathbf{X}_t \mid \mathbf{X}_{0: t-1}\right)=\mathrm{P}\left(\mathbf{X}_t \mid \mathbf{X}_{t-1}\right)$$
The current [[Zufallsvariable|Random Variable]] only depends on the previous random variable. The [[Markov-Kette|Markov Chain]] is an example of a first-order [[Markov Process]]. It has no memory.

**Second-order Markov Property:**
$$\mathrm{P}\left(\mathbf{X}_t \mid \mathbf{X}_{0: t-1}\right)=\mathrm{P}\left(\mathbf{X}_t \mid \mathbf{X}_{t-2}, \mathbf{X}_{t-1}\right)$$
The current [[Zufallsvariable|Random Variable]] only depends on the previous two random variables.

Increasing the order adds *memory* to the process. 

