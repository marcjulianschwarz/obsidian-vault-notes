---
uni-module: "KRY"
---

# b-adische Darstellung

Es sei $b\geq 2$ eine natürliche Zahl, dann lässt sich jede Zahl $n$ eindeutig schreiben als
$$n=\sum_{i=0}^{k-1} n_i \cdot b^i \quad \text { mit } \quad n_i \in\{0,1, \ldots, b-1\}$$
Ist $n_{k-1}\neq 0$ so nennt man $k$ die **Stellenzahl**.

Die Anzahl der Stellen kann man berechnen mit:
$$k=\left\lfloor\frac{\ln n}{\ln b}\right\rfloor+1$$

## Implementierung

In [[Python]]:

```python
bin(n) # Binärdarstellung einer Zahl
hex(n)
int(..., 2) # Dezimaldarstellung einer binären Zahl
int(..., 16)
```
