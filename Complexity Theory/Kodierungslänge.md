---
uni-module: LKO
---

# Kodierungslänge

Ist die Größe oder auch Länge einer [[Instanz]].
Die Anzahl der notwendigen Bits für eine Binärdarstellung der Instanz.

Für natürliche und ganze Zahlen:

$$
\begin{array}{ll}
\langle n\rangle=\left\lceil\log _{2}(n+1)\right\rceil & \text { für } n \in \mathbb{N} \\
\langle n\rangle=\left\lceil\log _{2}(|n|+1)\right\rceil+1 & \text { für } n \in \mathbb{Z}
\end{array}
$$

Für rationale Zahlen:
$$\langle r\rangle=\langle p\rangle+\langle q\rangle$$
