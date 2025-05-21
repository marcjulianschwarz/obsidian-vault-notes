---
uni-module: "LKO"

tags: Algorithmus
---

# Floyd-Warshall Algorithmus

Findet kürzeste Wege zwischen allen Knotenpaaren.
Findet negativen Kreis und gibt die zugehörigen Bögen aus.

![[Bildschirmfoto 2022-01-06 um 16.48.00.png]]

### JS

#infovislearn

```js
for (let k = 0; k < n; k++) {
  for (let i = 0; i < n; i++) {
    for (let j = 0; j < n; j++) {
      A[i][j] = Math.min(A[i][j], A[i][k] + A[k][j]);
    }
  }
}
```

## [[Laufzeit]]

$\mathcal{O}(n^3)$
