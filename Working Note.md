
I really want to try out cooking with Claude / Claude Code. Basically generating recipes based on a list of available ingredients. Take a look at this https://simonwillison.net/2025/Dec/23/cooking-with-claude/#atom-everything example and try it out. Then either add a note here or write a short blog post about the process. Maybe even connect this to my soon available recipes.marc-julian.com website.


Cool thing, I made a really nice tasting herbal butter with Claudes help:
- thyme
- rosmary (1:3 ratio with thyme)
- garlic
- salt
- butter

Tasted amazing.


## Bundle Chunk Size Improvements

Analyze bundle size using the rollup visualizer plugin in vite.config.ts:

```ts
import { visualizer } from "rollup-plugin-visualizer";

export default defineConfig({
  plugins: [
    react(),
    tailwindcss(),
    visualizer({
      filename: "stats.html",
      emitFile: true,
      template: "treemap",
    }),
  ],
  resolve: {
    alias: {
      "@": path.resolve(__dirname, "./src"),
    },
  },
});
```


Lazy import of pages:

```ts
const Page = lazy(() => import("./pages/page"));
```


This method can be used to lazily load components with large dependencies (e.g. PDFjs library). 