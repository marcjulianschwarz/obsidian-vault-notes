---
uni-module: "KRY"
---

# Diskreter Logarithmus

$$g^x=a \text { in } \mathbb{F}_p$$
$x$ heißt diskreter Logarithmus von $a$ zur Basis $g$ modulo $p$.

$x$ ist natürlich nur modulo der [[Ordnung]] von $g$ bestimmt, deswegen können wir $x$ auch direkt auf $0\leq x\leq \operatorname{ord}_p(g)-1$ beschränken.

Wenn $p$ eine [[Primzahl]] ist, dann ist die Gleichung genau dann lösbar, wenn
$$\operatorname{ord}_p(a)\mid \operatorname{ord}_p(g).$$

$g^x$ können wir sehr schnell mit der [[Square-And-Multiply-Methode zum Potenzieren|Square-And-Multiply-Methode]] berechnen. Wie kommen wir aber auf das richtige $x$ ?

Naive Berechnung

```python

```
