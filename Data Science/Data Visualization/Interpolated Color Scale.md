---
uni-module: "InfoVis"

tags: codesnippet, code, js, programmingassignment
---

# Interpolated Color Scale

[[Color Maps|Color Scale]]

Maps a value 𝑢∈[𝑢𝑚𝑖𝑛,𝑢𝑚𝑎𝑥]u∈[umin,umax] to a color based on a lookup-table. Values in between table-entries should be interpolated linearily in RGB color-space.

```js
// function colorscale() interpolate colors from a color lookup table
// @param  colors - array of colors - given as RGB triples
// @param  u - parameter at which color has to be interpolated
// @return  - triple containing the RGB color
function colorScale(colors, u, umin, umax) {
  if (u >= umax) return colors[colors.length - 1];
  if (u <= umin) return colors[0];
  const alpha = (u - umin) / (umax - umin);
  const nrColors = colors.length;
  const x = (nrColors - 1) * alpha;
  const i0 = Math.floor(x); // i0 >= due to line 9
  const i1 = i0 + 1; // i1 < nrColors due to line 8
  const dt = x - i0;
  const r = (1 - dt) * colors[i0][0] + dt * colors[i1][0];
  const g = (1 - dt) * colors[i0][1] + dt * colors[i1][1];
  const b = (1 - dt) * colors[i0][2] + dt * colors[i1][2];
  return [r, g, b];
}
```
