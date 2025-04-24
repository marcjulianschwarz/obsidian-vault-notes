---
uni-module: "InfoVis"

tags: programmingassignment
---

# Treemap - Slice and Dice Algorithm

```js
function sliceanddice(sibling, rect, depth) {
  let d = 0;
  sibling.forEach((s) => {
    if (depth % 2 === 0) {
      const w = s.size / rect.height;
      s.x = rect.x + d;
      s.y = rect.y;
      s.width = w;
      s.height = rect.height;
      d += w;
    } else {
      const h = s.size / rect.width;
      s.x = rect.x;
      s.y = rect.y + d;
      s.width = rect.width;
      s.height = h;
      d += h;
    }
  });
}
function treemap(node, depth) {
  if (hasChildren(node)) {
    const width = node.width;
    const height = node.height;
    const x0 = node.x;
    const y0 = node.y;
    const rect = { width: width, height: height, x: x0, y: y0 };
    const sibling = node.children;
    normalizeArea(sibling, rect);
    sliceanddice(sibling, rect, depth);
    sibling.forEach((n) => treemap(n, depth + 1));
  }
}
```
