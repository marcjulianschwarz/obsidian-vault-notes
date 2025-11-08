
There's this concept in aviation of "ahead of or behind the plane". When you're ahead of the plane, you understand completely what it's doing and why, and you're literally thinking in front of it. When you're behind the plane, it has done something expected and you are literally thinking behind it.

I think about coding assistants like this as well.

When I'm "ahead of the code," I know what I intend to write, why I'm writing it that way, etc. I have an intimate knowledge of both the problem space and the solution space I'm working in. But when I use a coding assistant, I feel like I'm "behind the code" - the same feeling I get when I'm reviewing a PR. I may understand the problem space pretty well, but I have to basically pick up the pieced of the solution presented to me, turn them over a bunch, try to identify why the solution is shaped this way, if it actually solves the problem, if it has any issues large or small, etc.


> For Juniors this is greatly raising their skill floor, as opposed to a senior where at best it's doing something they already can do, just faster. The elephant in the room being that if you aren't senior enough to have written the code you'll probably run into a catastrophic bug that you are incapable of fixing (or prompting the LLM to fix) very very quickly. Really it's just the next iteration of no-code hype where people dream of building apps without code, but then reality always come back to the fact that the essential skill of programmers is to understand and design highly structured and rigid logical systems. Code is just a means of specification. LLMs make it easier to leverage code patterns that have been written over and over by the hundreds of thousands of programmers that have contributed to its training corpus, but they can not replace the precision of thought needed to make a hand-wavy idea into a concrete system that actually behaves in a way that humans find useful.

I can relate with this comment above so much. When I don't have a clear plan in my mind and a clear mental model of the system I am trying to build, all [[Claude Code]] prompts just lead to a big old mess. This is going to be a skill that's really needed. Understanding how to create "structure" and "systems". And even better, understanding how to make them easy to use for other programmers (and today agents).


## Juniors

> Senior devs earned their experience of what is good/bad through **writing code**, understanding how hard and annoying it is to make a change, then **reworking those parts or making them better** the next time. The **feedback loop** was impactful because it was based on that code and them working with that code, so they knew exactly what the annoying parts are. Vibe-coding juniors do not know that, their conversation context knows that. Once things get buggy and changes are hard, they will fill up their context with tries/retries until it works, leading to their feedback loop being trained on prompts and coding tools, not code itself. Even if they read the outputted code, they have no experience using it so they are not aware of the issues - i.e. something would be better being a typed state, but they don't really use it so they will not care, as they do not have to handle the edge cases, **they will not understand the DX from an IDE**, they will not build a full [[Mental Model]] of how it works, just a shallow one. This leads to insane inefficiencies - wasting 50 prompt cycles instead of 10, not understanding cross-codebase patterns, lack of learning transfer from codebase to codebase, etc. With a minor understanding of state modeling and architecture, an vibe-coding junior can be made 100x more efficient, but **due to the vibe-coding itself, they will probably never learn state modeling and architecture, learn to refactor or properly manipulate abstractions**, leading to an eternal cycle of LLM-driven sloppypasta code, trained on millions of terrible github repositories, old outdated API's and stack overflow answers.
> "They will fill up their context with tries/retries until it works" Or until it does not. On numerous occasions I've observed LLMs get stuck in the endless loop of fix: one thing, break the other. Senior is capable of fixing it themselves and juniors may not even have a clue how the code works.

(bold parts highlighted by me)

> The worst possible situation is to have a non-programmer vibe code a large project that they intend to maintain. This would be the equivalent of giving a credit card to a child without first explaining the concept of debt.

## The craft of coding 

> I treat my coding as a craft. That has become much easier, since retiring. I'm quite aware that doing things my way isn't commercially viable, but no one pays me to do it. I do it for myself. That said, I find that it's important to always be challenging myself.
