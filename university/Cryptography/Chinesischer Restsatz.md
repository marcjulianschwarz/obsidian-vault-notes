---
uni-module: "KRY"

alias: "Chinesische Restsatz"
---

# Chinesischer Restsatz

Mit dem Chinesischen Restsatz lässt sich ein Gleichungssystem aus [[Kongruenz|Kongruenzen]] der folgenden Form lösen:

![[Bildschirm­foto 2023-02-26 um 14.54.13.png]]

wobei der [[Größter Gemeinsamer Teiler|ggT]] zwischen den $m_i, m_j$ immer gleich $1$ sein muss.

Eine [[Python]] Implementierung sieht so aus:

```python
def crt(a, m):
    M = np.prod(m)
    x = 0
    for ai, mi in zip(a, m):
        Mi = M / mi
        Ni = invmod(Mi, mi)
        x += ai * Mi * Ni
    return x % M
```

Für die Funktion `invmod` siehe [[Modulo Invertierbarkeit]].

Skript Seite 34, für $r=2$
