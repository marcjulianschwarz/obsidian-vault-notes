---
uni-module: "InfoVis"

tags: codesnippet, code, js, programmingassignment
---

# Hex To RGB

```js
function hexToRGB(hexStr) {
  const r = hexStr.substring(1, 3);
  const g = hexStr.substring(3, 5);
  const b = hexStr.substring(5, 7);

  return [Number("0x" + r), Number("0x" + g), Number("0x" + b)];
}
```
