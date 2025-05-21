---
uni-module: "InfoVis"
---

# Fruchterman and Reingold Algorithm

```js
const jiggle = () => (Math.random() - 0.5) * 1e-4;
const initDisplacements = (disp) => {
  for (let d of disp) {
    d.x = 0;
    d.y = 0;
    d.d = 0;
  }
};
const distance = (n1, n2) => {
  let dx = n2.x - n1.x;
  let dy = n2.y - n1.y;
  if (dx === 0) dx = jiggle();
  if (dy === 0) dy = jiggle();
  const l = Math.sqrt(dx * dx + dy * dy);
  return { x: dx / l, y: dy / l, d: l };
};
const attractingForce = (K, nodes, e, disp) => {
  const d = distance(nodes[e.source], nodes[e.target]); // vector pointing from n1 to n2
  const delta = d.d;
  const fa = (delta * Math.abs(delta)) / K;
  disp[e.source].x += fa * d.x;
  disp[e.source].y += fa * d.y;
  disp[e.target].x -= fa * d.x;
  disp[e.target].y -= fa * d.y;
};
const repulsiveForce = (K, nodes, i, j, disp) => {
  const d = distance(nodes[i], nodes[j]); // vector pointing from nodes[i] to nodes[j]
  const fr = (K * K) / d.d;
  disp[i].x -= fr * d.x;
  disp[i].y -= fr * d.y;
  disp[j].x += fr * d.x;
  disp[j].y += fr * d.y;
};
const step = (K, nodes, edges, bbox, disp, alpha) => {
  initDisplacements(disp);
  // compute displacements from repelling forces
  nodes.forEach((n, i) => {
    for (let j = i + 1; j < nodes.length; j++) {
      repulsiveForce(K, nodes, i, j, disp);
    }
  });
  // compute displacements from attracting forces
  edges.forEach((e) => {
    attractingForce(K, nodes, e, disp);
  });
  // update nodes position
  nodes.forEach(function (n, i) {
    const dx = disp[n.id].x;
    const dy = disp[n.id].y;
    const d = Math.sqrt(dx * dx + dy * dy);
    n.x += (dx / d) * Math.min(alpha, d);
    n.y += (dy / d) * Math.min(alpha, d);
    if (n.x < bbox.xmin) n.x = bbox.xmin;
    if (n.x > bbox.xmax) n.x = bbox.xmax;
    if (n.y < bbox.ymin) n.y = bbox.ymin;
    if (n.y > bbox.ymax) n.y = bbox.ymax;
  });
};
const fruchtermanReingold = (width, height, nodes, edges, bbox) => {
  const alphaMin = 15;
  const nrIterations = 200;
  const C = 0.46;
  const K = C * Math.sqrt((width * height) / nodes.length);
  const alphaDecay = (1 + alphaMin) / nrIterations;
  let alpha = 500;
  const disp = [];
  nodes.forEach((n, index) => disp.push({ d: 0, x: 0, y: 0, id: index }));
  let counter = 0;
  while (alpha >= alphaMin) {
    // one simulation step
    step(K, nodes, edges, bbox, disp, alpha);
    // cooling
    alpha -= alphaDecay;
    counter++;
  }
  return counter;
};
```
