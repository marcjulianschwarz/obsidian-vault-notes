---
uni-module: "KRY"
---

# Modulo Invertierbarkeit

Das Konzept der [[Invertierbarkeit]] aber mit [[Modulo]].

Wir nennen $b$ ein Inverses von $a$ modulo $n$, wenn gilt:
$$ab\equiv 1\bmod n.$$

Wir wissen $a$ ist genau dann invertierbar modulo $n$ wenn
$$ggT(n, a)=1.$$

Wir berechnen also mit dem [[Erweiterter Euklidischer Algorithmus]] $x$ und $y$, sodass $xn+ya=1$.
Wir wissen $$ya\equiv1\bmod n \quad = \quad n|ya-1.$$
Außerdem wissen wir
$$ya-1=-xn$$
und
$$n|xn$$
, da $xn$ ein Vielfaches von $n$ ist.
Es ist also $y$ invers zu $a$ mod $n$ eindeutig.

Ein kurzes Beispiel in [[Python]]:

```python
n = 101
a = 37

ggt, x, y = eea(n, a)
if ggt == 1:
    print((y * a) % n)
    print(y % n)
    # y is invers to a mod n
    # 71 is invers to 37 mod 101
```
