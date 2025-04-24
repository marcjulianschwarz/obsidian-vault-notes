---
uni-module: "InfoVis"

tags: codesnippet, code, js, programmingassignment
---
# Interpolated Color Scale HSV

The function should map an item-value in $[0,1]$ to a hex-color-string. The color should be the linear interpolation of bright-white (at item-value = 0.5) and the completely saturated colors given by ℎ𝑢𝑒𝑚𝑖𝑛, ℎ𝑢𝑒𝑚𝑎𝑥 and 𝑣𝑎𝑙𝑢𝑒𝑐𝑜𝑛𝑠𝑡 in [[HSV Color Model]] [[Color Space]].

```js
/** function hsv_to_color_string( h, s, v ): converts a color given by 3 numbers
 *        h in [0,360],  s and v in [0,1]   to a hex-color-string
 */
/** mapColors
 * @param    value  item-value ranging from 0 to 1.
 * @param    hue_min  hsv-hue for the color of the minimal value
 * @param    hue_max  hsv-hue for the color of the maximal value
 * @param    value_const  hsv-value for both of the minimal and maximal value-colors
 * @return   hex-color-string, representing the color for the given value.
 */
function mapColor(value, hue_min, hue_max, value_const) {
  const h = value < 0.5 ? hue_min : hue_max;
  const s = Math.abs(value - 0.5) * 2;
  const v = 1 - (1 - value_const) * Math.abs(value - 0.5) * 2;
  return hsv_to_color_string(h, s, v);
}
```
