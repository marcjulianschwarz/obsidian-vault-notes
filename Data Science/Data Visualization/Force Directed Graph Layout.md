---
uni-module: "InfoVis"

alias: ["Spring Embedding", "Spring-Electric Layout"]
---

# Force Directed Graph Layout

- computes layout for simple [[Ungerichteter Graph|Undirected Graph]]
- uses structural information from the [[Network]]
- usually crossing-free for [[Planarer Graph|Planar Graph]]
- [[Community Structure]] becomes visible
- repulsive force between nodes and attracting force between connected nodes

## Limits

- slow
- only [[Euklidische Norm|Euclidean Distance]]

[[Hook's Law]]
[[Electric Force]]

The total force acting on a node $f_t$ is given by the vector sum of an **attracting** component $f_a$ , the spring force and a **repulsive** component $f_r$ :
$$f_t=f_a+f_r$$
for [[Electric Force]].

## Algorithms

- [[Eades Algorithm]]
- [[Fruchterman and Reingold Algorithm]]
- [[ForceAtlas2]]

![[Bildschirmfoto 2022-09-03 um 11.51.58.png]]
