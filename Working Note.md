
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


## UX Design


- document flows from apps I really like. Thinking of journeys not of screens
	- generally try to understand flows, structured steps in a user journey
- write down design decision. Why did I design it like this?
- show to small user base (5 users or so)
- don't but icons in menus everywhere, use them where they make sense
- Explore well-known components from different websites: https://component.gallery/components/


## AI Features 

Don't make them boring like a chat or search feature. Make them fit right in and automatically do stuff without the user even noticing that it is AI.

# Anticipatory shipping

No idea why but I found out about this patent from Amazon that kind of blows my mind. If you display strong intent to buy a certain product, Amazon will already load the item on a truck and move it  to a logistics center near you. On a large scale this will more often than not actually be the right decision. 


## Cool CLI Website stuff

About me:

```bash
curl marc-julian.com
```

Contact me:

```bash
curl marc-julian.com/email | sh
```

## 3D Printing

Want to get into 3D printing again. And I found a cool thing that I would like to print. This espresso single shot glass holder:

![[CleanShot 2026-01-19 at 17.02.55@2x.png]]

You can attach this to a wall and always have the perfect amount of coffee (fresh beans or preground) ready to go. See [the-brew-code.de](https://the-brew-code.de) for my coffee obsession.


## Product Marketing

Build things and then talk about them in a way that people remember and share it with friends. I guess some call it clever product marketing.


## Reading

I want to get into the habit of reading books aloud. This helps a lot in being attentive and actually understanding the written words. And it will let you come up with tons of questions about the text and your understanding of it.
