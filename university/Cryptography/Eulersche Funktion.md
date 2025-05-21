---
uni-module: "KRY"
---

# Eulersche Funktion

Die Anzahl an $a$ zwischen $0$ und $n$, für die gilt, dass der [[Größter Gemeinsamer Teiler|ggT]] mit $n$ gleich $1$ ist.

$$\varphi(n)=\#\{a: 0 \leq a \leq n-1, \operatorname{ggT}(a, n)=1\}=\#(\mathbb{Z} / n \mathbb{Z})^*$$

Einfache Implementierung in [[Python]]:

```python
def euler(n):
    c = 0
    for a in range(n):
        ggt, _ = ggT(a, n)
        if ggt == 1:
            c += 1
    return c
```

Dieser Algorithmus ist sehr langsam für großes $n$. Mit dem [[Naives Faktorisierungsverfahren|naiven Faktorisierungsverfahren]] lässt sich die eulersche Funktion auch wie folgt bestimmen:
$$\varphi(n)=\prod_i p_i^{e_i-1}\left(p_i-1\right)=n\left(1-\frac{1}{p_1}\right) \ldots\left(1-\frac{1}{p_r}\right)=n \prod_{p \mid n}\left(1-\frac{1}{p}\right)$$

Kann auch verwendet werden um zu testen ob eine Zahl $n$ eine [[Primzahl]] ist. Man testet:
$$\varphi(n)=n-1.$$
Also in Python:

```python
def is_prime(n):
	return euler(n) == n-1
```

Für $n$ gelten die folgenden Äquivalenzen:

$$n \text { ist Primzahl } \Longleftrightarrow \varphi(n)=n-1 \quad \Longleftrightarrow \mathbb{Z} / n \mathbb{Z} \text { ist Körper. }$$
[[Körper]]

Wenn $n$ keine [[Primzahl]] ist, dann haben wir
$$n=ab.$$
Damit gilt also in
$$\mathbb{Z}/n \mathbb{Z}$$
, dass $ab=0$ wobei $a\neq 0$ und $b\neq 0$. Es ist also kein [[Integritätsring]]
