---
uni-module: KRY
tags:
  - Algorithmus
---

# Naives Faktorisierungsverfahren

Ein naiver (exponentieller) Ansatz zur Faktorisierung von einer Zahl $n$ in ein Produkt aus [[Primzahl|Primzahlen]].

## [[Python]] Implementierung

````python
def naive_factorization(n):
    # First count number of times n is divisible by 2
    if n % 2 == 0:
        e = 1
        n = n / 2
        while n % 2 == 0:
            e += 1
            n = n / 2
        yield {2: e}
    # Then start with bases bigger than 2
    p = 3
    while p**2 <= n: # Test if p <= sqrt(n)
        if n % p == 0:
            e = 1
            n = n / p
            # count number of times divisible by p
            while n % p == 0:
                e += 1
                n = n / p
            yield {p: e}
        p = p + 2
    # If n is not 1, then n is prime
    if n > 1:
        yield n

list(naive_factorization(12))```


Induziert einen Primzahlbeweis. Wenn man keinen Teiler $t\leq\sqrt{n}$ findet, dann ist $n$ [[Primzahl]].

## [[Laufzeit]]
$$\mathcal{O}(\sqrt{n}\ln^2{n})$$
und damit exponentiell.
````
