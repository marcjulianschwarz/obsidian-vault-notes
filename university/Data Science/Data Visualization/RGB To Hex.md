---
uni-module: "InfoVis"

tags: codesnippet, code, js, programmingassignment
---

# RGB To Hex

```js
function rgbToHex(color) {
  const r = color[0];
  const g = color[1];
  const b = color[2];
  const hex = "#" + r.toString(16).padStart(2, "0") + g.toString(16).padStart(2, "0") + b.toString(16).padStart(2, "0");
  return hex;
}
```
