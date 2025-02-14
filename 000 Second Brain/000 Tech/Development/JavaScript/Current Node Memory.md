```ts
const memory = process.memoryUsage();
console.log((memory.heapUsed / 1024 / 1024 / 1024).toFixed(4), "GB");
```
