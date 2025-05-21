---
uni-module: "InfoVis"
---

# Word Cloud

Visualizes word frequency.

- tag size
- users scan and not read a word cloud
- centering
- position → upper left quadrant more important
- exploration suboptimal

## Tools

- [Word cloud generator, Jason Davies (see picture on the left)](https://www.jasondavies.com/wordcloud/)
- [Wortwolken.com](https://www.wortwolken.com/)
- [Word Art](https://wordart.com/)
- [Tagxedo](http://www.tagxedo.com/)

## Algorithm

#programmingassignment

```js
// Word Cloud
// Use the functions:
//  - randomizePosition( word ) to generate a random position for the word in the drawing area
//  - getAabb( word ) to compute the AABB for the input word
//  - aabbsIntersect( aabb_a, aabb_b ) to test two AABBs for intersection
// @param {Array} words, array of word objecs. A word has the properties
//  const word = {
//     x: x_coord,
//     y: y_coord,
//     width: word_width,
//     height: word_height,
//     insertion_failed: boolead // indicates if the word was included in the word cloud
//     /** more attributes not required by the assignment */
//  }
function wordcloud(words) {
  const aabbs = [];
  function intersectsAny(aabb) {
    for (let b of aabbs) {
      if (aabbsIntersect(aabb, b)) return true;
    }
    return false;
  }
  for (let w of words) {
    w.insertion_failed = true;
    for (let i = 0; i < 1000; ++i) {
      randomizePosition(w);
      const aabb = getAabb(w);
      if (!intersectsAny(aabb)) {
        aabbs.push(aabb);
        w.insertion_failed = false;
        break;
      }
    }
  }
} // wordcloud
```
