---
uni-module: "InfoVis"
---

# Stream Graph

Can be used to visualize multiple time series at the same time (cumulative).

## Algorithm

```js
const offsetBase = (data) => {
  return new Array(data[0][1].length).fill(0);
};
const offsetSymmetric = (data) => {
  const g0 = new Array(data[0][1].length).fill(0);
  for (let l of data) {
    // the layers
    for (let [i, t] of l[1].entries()) {
      g0[i] += t.n;
    }
  }
  for (let i = 0; i < g0.length; i++) {
    g0[i] /= -2;
  }
  return g0;
};
const offsetWiggle = (data) => {
  const n = data.length; // this is the number of layers
  const g0 = new Array(data[0][1].length).fill(0);
  for (let [j, l] of data.entries()) {
    // the layers, j is the index of the time series
    for (let [i, t] of l[1].entries()) {
      g0[i] += (n - j) * t.n; // n-(j+1) + 1, start with j=0
    }
  }
  for (let i = 0; i < g0.length; i++) {
    g0[i] /= -(n + 1);
  }
  return g0;
};
const t_ = (data, g0, ts0) => {
  // init
  for (let [j, l] of data.entries()) {
    ts0.push([]);
    ts0[j] = [];
    for (let [i, e] of l[1].entries()) {
      const d = [g0[i], g0[i] + e.n, e.year, e.n, e.name];
      ts0[j].push(d);
      g0[i] += e.n;
    }
  }
};
const timeSeries = (data, ts0, ts1, ts2) => {
  // compute base case
  const g0Base = offsetBase(data);
  const g0Symmetric = offsetSymmetric(data);
  const g0Wiggle = offsetWiggle(data);
  t_(data, g0Base, ts0);
  t_(data, g0Symmetric, ts1);
  t_(data, g0Wiggle, ts2);
};

// collect data
const minYear = 1950;
const bnames = [];
data.forEach((e) => {
  if (+e.year >= minYear) {
    const item = { year: +e.year, n: +e.n, name: e.name, gender: e.sex };
    bnames.push(item);
  }
});
// compute min and max years
const minX = bnames.reduce((a, b) => (a.year < b.year ? a : b)).year; // this is actually minYear
const maxX = bnames.reduce((a, b) => (a.year > b.year ? a : b)).year;
// compute layers
const s_ = new Set();
bnames.forEach((n) => {
  s_.add(n.name);
});
const m_ = new Map();
for (const entry of s_.entries()) {
  const e = [];
  for (let i = minX; i <= maxX; i++) {
    e.push({ year: i, name: entry[0], n: 0, gender: entry[1] });
  }
  m_.set(entry[0], e);
}
bnames.forEach((n) => {
  m_.get(n.name)[n.year - minX] = n;
});
// data must an array
// create time in all tree modes
const ts0 = [];
const ts1 = [];
const ts2 = [];
//timeSeries(Array.from(m_),ts0,ts1,ts2)
timeSeries(Array.from(new Map([...m_.entries()].sort())), ts0, ts1, ts2);
```

## Programming Assignments

#programmingassignment

### Base Offset

```js
/** Stream Graph Base Offset
 * The input is an array of arrays containing the time series. In order to access
 * a time series j at a given time step i write t[i][j]
 * @param{number[[]]} t array of arrays containing the time series
 * @return {number[]} array containing the baseline
 */
function offsetBase(t) {
  const baseOffset = [];
  t.forEach((e) => baseOffset.push(0));
  return baseOffset;
} // baseOffset()
```

### Symmetric Silhouette

```js
/** Stream Graph - Symmetric silhouette (ThemeRiver)
 * The input is an array of arrays containing the time series. In order to access
 * a time series j at a given time step i write t[i][j]
 * @param {Number[[]]} t array of arrays containing the time series
 * @return {Number[]} array containing the baseline
 */
function symmetricSilhouette(t) {
  const g0 = new Array(t.length).fill(0);
  t.forEach((e, i) => {
    const n = e.length;
    e.forEach((l, j) => {
      g0[i] += l;
    });
    g0[i] /= -2;
  });
  return g0;
} // symmetricSilhouette()
```

### Wiggle

```js
/** Stream Graph - wiggle layout: minimize deviation
 * The input is an array of arrays containing the time series. In order to access
 * a time series j at a given time step i write t[i][j]
 * @param {Number[[]]} t - array of arrays containing the time series
 * @return {Number[]} array containing the baseline
 */
function wiggle(t) {
  const g0 = new Array(t.length).fill(0);
  t.forEach((e, i) => {
    const n = e.length;
    e.forEach((l, j) => {
      g0[i] += (n - j) * l; // n - (j+1) + 1, start with index 0
    });
    g0[i] /= -(n + 1);
  });
  return g0;
} // wiggle()
```
