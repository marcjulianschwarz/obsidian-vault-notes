
```js
window.onblur = window.onfocus = () => {
  window.document.title = document.visibilityState == "visible" ? "O" : "O";
};
```
