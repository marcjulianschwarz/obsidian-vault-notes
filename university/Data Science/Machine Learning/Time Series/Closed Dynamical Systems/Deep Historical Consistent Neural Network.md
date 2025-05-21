---
uni-module: "MBNN"

alias: ["Deep HCNN", "DHCNN", "DHCNNs", "Deep HCNNs"]
---

# Deep Historical Consistent Neural Network

## A simple approach

Stack multiple [[Historical Consistent Neural Network|HCNNs]] and connect them via their hidden states.

![[Bildschirm­foto 2023-06-08 um 13.38.39.png]]

use the more complicated state transformation

$$
\begin{aligned}
\left(\begin{array}{c}
s^{\prime \prime} \\
s^{\prime} \\
s
\end{array}\right)_\tau=\tanh \left[\left(\begin{array}{ccc}
A^{\prime \prime} & C^{\prime} A^{\prime} & 0 \\
0 & A^{\prime} & C A \\
0 & 0 & A
\end{array}\right) \cdot\left(\begin{array}{l}
s^{\prime \prime} \\
s^{\prime} \\
s
\end{array}\right)_{\tau-1}+\left(\begin{array}{l}
0 \\
0 \\
B
\end{array}\right) u_t\right] \\
y_\tau=\left(\begin{array}{lll}
D & 0 & 0
\end{array}\right)\left(\begin{array}{c}
s^{\prime \prime} \\
s^{\prime} \\
s
\end{array}\right)_\tau
\end{aligned}
$$

to calculate the next states.
