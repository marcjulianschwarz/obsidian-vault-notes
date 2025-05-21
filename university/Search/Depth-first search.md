---
uni-module: "LKO"

tags: "Algorithmus"
---

# Depth-first search

- finds connected [[Zusammenhangskomponente|Components]]
- searches an element in a [[Baum|Tree]] or [[Network]]
- computes a [[Aufspannender Baum|Spanning Tree]]
- **BUT** it does **not** find the shortest path in an unweighted [[Graph]]

## Algorithm

![[Bildschirmfoto 2022-01-06 um 15.46.53.png]]

_next_ = Anzahl der [[Zusammenhangskomponente | Zusammenhangskomponenten]]
_mark_ = Array wo die gleiche Zahl immer die gleiche Komponente bedeutet

## Laufzeit

Die [[Laufzeit]] ist $\mathcal{O}(|V|+|E|)$.

## [[Python]] Implementierung

```python
def depth_search(g):
	mark = [-1 for i in g.nodes]
	next = 0

	for v in g.nodes:
		if mark[v] < 0:
			next = next + 1
			mark[v] = next
			for w in v.neighbors:
				# Rekursiv:
				checkNeighbor(w, next)
	return next, mark
```

```python
def checkNeighbor(w, next):
	if mark[w] = next
		for u in w.neighbors:
			checkNeighbor(u, next)
```

## JavaScript Implementierung

Verwendet einen [[Stack]] und funktioniert dementsprechend eigentlich genauso wie [[Breadth-first search]] wobei die [[Queue]] einfach durch einen [[Stack]] ersetzt wurde.

```javascript
// nodes: array of input nodes
// neighbors: array of array of neighbors
// index: index of source node
const dfs = (nodes, neighbors, index) => {
  // initialize
  nodes.forEach((n) => {
    n.v = false; // not visited
    n.d = Infinity;
    n.p = -2; // any non-valid predecessor
  });
  // init source node
  nodes[index].d = 0;
  nodes[index].p = -1;
  const q = [index]; // queue, use as LIFO (stack)
  // main loop
  while (q.length > 0) {
    const s = q.pop();
    const d = nodes[s].d;
    if (!nodes[s].v) {
      nodes[s].v = true;
      neighbors[s].forEach((n) => {
        if (!nodes[n].v) {
          nodes[n].p = s;
          nodes[n].d = d + 1;
          q.push(n);
        }
      });
    }
  } // while
}; // end dfs()
```
