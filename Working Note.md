
Maybe add the following to my working/coding principles:
- **The ability to accurately answer questions about large software systems is extremely valuable**. -> Striving to be able to do that

## Documenting healthy diet habits 

This is only a quote that got me thinking about it:

> Eat lots of fruits and vegetables. Avoid processed food. Especially avoid processed meats. Eat food with low caloric density. Avoid added sugar. Avoid alcohol. _Avoid processed food_.

But I really want to summarize all my gained knowledge about a healthy diet somewhere (maybe on recipes.marc-julian.com or in a note here). Just to have everything in one place.
## Blog Post Titles Checklist

- [ ] Do the potential readers understand it?
- [ ] Does it NOT rely on a well established personal brand?
- [ ] Do I want to be a bit informal? Show it in the title.
- [ ] Don't have the conclusion in your title
- [ ] Don't have a title be just a "label" like "The XYZ Effect"
- [ ] Make the title be a short sentence 
- [ ] Start to create your thing, _then_ you choose a title, then structure your thing to deliver on the title 

## On Independence

Want to form this into some actionable points:
https://collabfund.com/blog/pure-independence/


## Social Media and other free dopamine as a local minima

Read the following comment on a Hackernews discussion some time ago and I resonate with this description of "free dopamine hits" like social media being a local minimum. It is really easy to end up in this place of a social media addiction but it requires significant effort to overcome the slope out of this minimum to get over the edge down into a more global or better minimum. 

Now the question is, how do you find the slope, how do you start climbing it and how do you avoid falling back down while climbing it.

> Fundamentally, I think having a source of "free dopamine" on tap is not going to do any good. If I can get distracted from my real world tasks anytime, anywhere, the immediate incentives to work on real things disappear. Effectively, one can get stuck in a local minimum.
> I don't know how to solve it, but personally I've chosen to block as many feeds/algorithms as I can, so I have to make a conscious decision to search for something (making it just as hard as making the conscious decision that I'm likely putting off). The only feeds I have right now are the FT and Hacker News. Everything else is just a blank home screen with a search bar.

## Effort

Something I want to try to do is doing things with less effort, like explained in [this post](https://expandingawareness.org/blog/the-appropriate-amount-of-effort-is-zero/). This does not mean being lazy but just doing things a bit more laid back. 
This reminds me a lot of this concept I always encountered while doing Cardistry, Speedcubing, Speedstacking and Poiball:

> Do it slow. Slow is **smooth** and smooth is **fast**.

Maybe this is even relevant in the context of AI Assisted coding ([[Thoughts on AI assisted coding]]) where people (including me) tend to crank out feature by feature without stepping back and taking the time to fully grasp the problem first. Something to think about for sure.

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
