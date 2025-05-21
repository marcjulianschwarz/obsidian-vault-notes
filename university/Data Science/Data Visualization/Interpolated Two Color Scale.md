---
uni-module: "InfoVis"

tags: codesnippet, code, js, programmingassignment
---

# Interpolated Two Color Scale

The function maps an item-value in $[0,1]$ to a hex-color-string. The color should be the linear interpolation in RGB [[Color Space]] of the two given rgb-color tuples 𝑐𝑚𝑖𝑛 and 𝑐𝑚𝑎𝑥. The formula for linear Interpolation of two scalar values 𝑎 and 𝑏 at the parameter value $t\in [0,1]$ is $c=a(1-t)+bt$.

```js
/**
 * function rgb_vector_to_color_string( vec3 ): converts a color given by an array of length 3
 *           vec3 = [r,g,b] each in [0,1]       to a hex-color-string
 */

/**
 * mapColors
 * @param     item-value ranging from 0 to 1.
 * @param{number[3]} c_min   array of 3 numbers, each in [0,1], rgb-color for the minimal value
 * @param{number[3]} c_max   array of 3 numbers, each in [0,1], rgb-color for the maximal value
 * @return   hex-color-string, representing the color for the given value.
 */

function mapColor(value, c_min, c_max) {
  function lerp(a, b, t) {
    return (1 - t) * a + t * b;
  }
  let vec = [lerp(c_min[0], c_max[0], value), lerp(c_min[1], c_max[1], value), lerp(c_min[2], c_max[2], value)];
  return rgb_vector_to_color_string(vec);
}
```
