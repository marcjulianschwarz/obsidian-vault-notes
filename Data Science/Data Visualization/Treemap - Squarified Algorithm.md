---
uni-module: "InfoVis"

tags: programmingassignment
---

# Treemap - Squarified Algorithm

## Main Loop

```js
function treemap(node) {
  if (hasChildren(node)) {
    const width = node.data.width;
    const height = node.data.height;
    const x0 = node.data.x;
    const y0 = node.data.y;
    const rect = { width: width, height: height, x: x0, y: y0 };
    const sibling = node.children;
    normalizeArea(sibling, rect);
    squarified(
      sibling.sort((a, b) => {
        return b.value - a.value;
      }),
      [],
      rect
    );
    sibling.forEach((n) => treemap(n));
  }
}
```

## Layout a row

```js
function squarified(sibling, row, rect) {
  // check if level was processed and layout it
  if (sibling.length === 0) {
    if (row.length > 0) {
      layoutrow(row, rect);
    }
    return;
  }
  // test if node can be inserted into row, otherwise layout row
  let node = sibling[0];
  if (row.length === 0) {
    row.push(node);
    squarified(sibling.slice(1), row, rect);
  } else {
    if (aspectRatios(row, node, rect)) {
      // insert node into row
      row.push(node);
      squarified(sibling.slice(1), row, rect);
    } else {
      //start a new row
      layoutrow(row, rect);
      squarified(sibling, [], rect);
    }
  }
}
```

## Algorithm

```js
function normalizeArea(sibling, rect) {
  const totArea = rect.width * rect.height;
  let totWeight = 0;
  sibling.forEach((s) => {
    totWeight += s.size;
    s.weight = s.size;
  });
  const factor = totArea / totWeight;
  sibling.forEach((c) => {
    c.size = factor * c.size;
  });
}
function aspectRatios(row, node, rect) {
  const h = rect.width < rect.height ? rect.width : rect.height;
  const a = [];
  let totA = 0;
  row.forEach((r) => {
    a.push(r.size);
    totA += r.size;
  });
  let maxAspectRatio1 = 0;
  a.forEach((ai) => {
    const r = Math.max((h * h * ai) / (totA * totA), (totA * totA) / (h * h * ai));
    maxAspectRatio1 = r > maxAspectRatio1 ? r : maxAspectRatio1;
  });
  let maxAspectRatio2 = 0;
  a.push(node.size);
  totA += node.size;
  a.forEach((ai) => {
    const r = Math.max((h * h * ai) / (totA * totA), (totA * totA) / (h * h * ai));
    maxAspectRatio2 = r > maxAspectRatio2 ? r : maxAspectRatio2;
  });
  return maxAspectRatio1 > maxAspectRatio2;
}
function layoutrow(row, rect) {
  let totA = 0;
  row.forEach((e) => {
    totA += e.size;
  });
  let x = rect.x;
  let y = rect.y;
  let w = 0;
  let h = 0;
  if (rect.width < rect.height) {
    row.forEach((e) => {
      w = (e.size * rect.width) / totA;
      h = e.size / w;
      e.x = x;
      e.y = y;
      e.width = w;
      e.height = h;
      x += w;
    });
    rect.y += h;
    rect.height -= h;
  } else {
    row.forEach((e) => {
      h = (e.size * rect.height) / totA;
      w = e.size / h;
      e.x = x;
      e.y = y;
      e.width = w;
      e.height = h;
      y += h;
    });
    rect.x += w;
    rect.width -= w;
  }
}
function squarified(sibling, row, rect) {
  if (sibling.length === 0) {
    if (row.length > 0) {
      layoutrow(row, rect);
    }
    return;
  }
  let node = sibling[0];
  if (row.length === 0) {
    row.push(node);
    squarified(sibling.slice(1), row, rect);
  } else {
    if (aspectRatios(row, node, rect)) {
      row.push(node);
      squarified(sibling.slice(1), row, rect);
    } else {
      layoutrow(row, rect);
      squarified(sibling, [], rect);
    }
  }
}
function treemap(node) {
  if (hasChildren(node)) {
    const width = node.width;
    const height = node.height;
    const x0 = node.x;
    const y0 = node.y;
    const rect = { width: width, height: height, x: x0, y: y0 };
    const sibling = node.children;
    normalizeArea(sibling, rect);
    squarified(
      sibling.sort((a, b) => b.size - a.size),
      [],
      rect
    );
    sibling.forEach((n) => treemap(n));
  }
}
```

Python Library:
https://github.com/laserson/squarify#Usage
