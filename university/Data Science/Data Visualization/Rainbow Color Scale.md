---
uni-module: "InfoVis"

tags: codesnippet, code, programmingassignment, js
---

# Rainbow Color Scale

Map a fixed set of item-values to different colors given by a scalar rainbow [[Color Maps|Color Scale]]. Use the [[HSV Color Model]] [[Color Space]] and choose appropriate values. Note that, the ends of the scale should be distinguishable.

```js
/** mapColor(): linear interpolation from [0,1] to [0, maxHue]
 * @param {Number} u in [0, 1], value that should be mapped to hue in the HSV color model
 * @param {Number} maxHue, maximum value of hue
 * @return {Array} [h,s,v], hue, saturation and value of the color in the HSV color model
 *                 set s = 0.8, and v = 0.9
 */
function mapColor(u, maxHue) {
  const s = 0.8;
  const v = 0.9;
  return [u * maxHue, s, v];
}
```
