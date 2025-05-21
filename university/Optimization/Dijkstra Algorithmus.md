---
uni-module: EMD, LKO

tags: Algorithmus
---
→ [[Graphengenerierung]]

# Dijkstra Algorithmus

Mit dem Dijkstra Algorithmus lässt sich der minimale Pfad zwischen zwei Knoten in einem [[Graph]] bestimmen.

## Algorithm

![[Bildschirmfoto 2022-01-06 um 16.40.06.png]]

## [[Laufzeit]]

Best-Case ([[vollständig]]) : $\mathcal{O}(n^2)$
Best-Case ([[Sparsity|sparse]]) : $\mathcal{O}(m+n\log{n})$ (uses Fibonacci [[Heap]])

## [[Python]] Implementierung

```python

```

## JavaScript Implementierung

verwendet Priority Queue als Fibonacci Heap.

#infovislearn

```js
/********************************************************************************************
 * Dijkstra
 *    Computes distance of all nodes to source node.
 *    Requires the use of a priority queue. This implementation
 *    uses heap-js
 */
const dijkstra = (nodes, neighbors, index) => {
  const pQ = new heap.Heap((a, b) => {
    return a.d - b.d;
  });
  nodes.forEach((n) => {
    n.v = false;
    n.d = Infinity;
    n.p = -2; // invalid predecessor
  });
  nodes[index].d = 0;
  nodes[index].v = true;
  nodes[index].p = -1; // root or source node
  nodes.forEach((n) => pQ.add(n));
  while (!pQ.isEmpty()) {
    const s = pQ.pop();
    s.v = true;
    const d = s.d;
    neighbors[s.index].forEach((e) => {
      const n = nodes[e.id];
      if (n.v === false) {
        // element still in the queue
        if (d + e.weight < n.d) {
          // update this element
          n.p = s.index;
          n.d = d + e.weight;
          // update priority queue
          pQ.remove(n);
          pQ.add(n);
        }
      }
    });
  }
};
```

---

1. Startknoten auswählen mit Distanz 0
2. Alle anderen Knoten haben Distanz unendlich

→ Beweis zur Korrektheit anschauen (für Klausur)
