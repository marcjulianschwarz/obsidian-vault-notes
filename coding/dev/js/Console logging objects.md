
Better way to console log complex objects:

```js
console.dir(object, { 
  depth: Infinity,
  colors: true,
  numericSeparator: true
});
```

