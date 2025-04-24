---
uni-module: "LKO"
tags: Algorithmus, codesnippet, code, js, Python
---

# Breadth-first search

- shortest path between a source node and all other nodes in unweighted [[Graph]]
- finds connected [[Zusammenhangskomponente|Components]]
- computes a [[Aufspannender Baum|Spanning Tree]]
- path to source node can be recondstructed by backtracking

## Algorithm

![[Bildschirmfoto 2022-01-06 um 15.56.31.png]]

_next_ = Anzahl der [[Zusammenhangskomponente | Zusammenhangskomponenten]]
_mark_ = Array wo die gleiche Zahl immer die gleiche Komponente bedeutet

## Laufzeit

Die [[Laufzeit]] ist $\mathcal{O}(|V|+|E|)$.

## [[Python]] Implementierung

```python
def breadth_search(g):
	mark = [-1 for i in g.nodes]
	next = 0
	L = []

	for v in g.nodes:
		if mark[v] < 0:
			next = next + 1
			L.append(v)

			while L != 0:
				v = L.shift()
				if mark[v] < 0:
					mark[v] = next

				for w in v.neighbors:
					if mark[w] < 0:
						mark[w] = next
						L.append(w)
	return next, mark
```

## JavaScript Implementierung:

Verwendet eine [[Queue]].

```javascript
// nodes: array of _nodes
// neighbors: array of array of neighbors for all nodes
// index: index of source node
const bfs = (nodes, neighbors, index) => {
  nodes.forEach((n) => {
    n.v = false; // visited -> false
    n.d = Infinity;
    n.p = -2; // any non-valid predecessor
  });
  nodes[index].d = 0;
  nodes[index].v = true;
  nodes[index].p = -1; // source node has predecessor -1
  const q = [index]; // queue
  while (q.length > 0) {
    const s = q.shift();
    const d = nodes[s].d;
    neighbors[s].forEach((e) => {
      const n = nodes[e];
      if (n.v === false) {
        n.v = true;
        n.p = s;
        n.d = d + 1;
        q.push(n.index);
      }
    });
  } // end while
}; // end bfs()
```
