
These are somewhat up to date opinions and thoughts I have about AI assisted coding / vibe coding.

## Value of Coding

I don't think there is a value shift in coding. The true value lies in judgment, tradeoffs, and intent. And it always has.


## Synthetic competence

> In the old world, not understanding something showed up as not being able to build it. Now the building is cheap, and understanding has to be checked some other way: by whether the person can predict how the thing fails, name the assumptions it’s making

> The user gets better at producing confident output and worse at telling whether it’s right, and that widening ratio is where the damage piles up, quietly, one accepted answer at a time.

https://www.jonathanbeard.io/blog/2026/06/27/the-80-percent-problem.html


## 80% Problem

The last 20%:
- Edge Cases 
- Failure Modes
- Operational Realities

https://www.jonathanbeard.io/blog/2026/06/27/the-80-percent-problem.html


## Skill Atrophy

> Automate the easy eighty percent, leave the human the hard twenty, then remove the very practice that built competence at the hard part to begin with.

> The developer who shifts from writing code to reviewing generated pull requests loses the daily reps that built the instinct to spot a race condition or a security hole on sight, and the review gets worse as the instinct fades. Skills that go unused decay, so the people best positioned to catch a truly wrong output are slowly becoming the least practiced at the underlying work. And here’s the deepest one, because it’s generational: today’s senior engineers, the ones qualified to supervise the machine, earned that judgment by grinding through the boilerplate and the edge cases themselves, back when that was simply the job.

Scary to think of it this way...

https://www.jonathanbeard.io/blog/2026/06/27/the-80-percent-problem.html

## Human brain catching up with the speed of coding agents

> There's this concept in aviation of "ahead of or behind the plane". When you're ahead of the plane, you understand completely what it's doing and why, and you're literally thinking in front of it. When you're behind the plane, it has done something expected and you are literally thinking behind it.

Often I feel like this. The speed at which agents can generate code is too fast to actually catch up. 
If we consider judgment, tradeoff and especially intents as the value in coding, then it seems important to me that you are always ahead of the agent.

#todo how can we catch up with agents? 

Maybe we should spent a lot more time planning ahead and reviewing code to counteract this information imbalance. 

> When I'm "ahead of the code," I know what I intend to write, why I'm writing it that way, etc. I have an intimate knowledge of both the problem space and the solution space I'm working in. But when I use a coding assistant, I feel like I'm "behind the code" - the same feeling I get when I'm reviewing a PR. I may understand the problem space pretty well, but I have to basically pick up the pieced of the solution presented to me, turn them over a bunch, try to identify why the solution is shaped this way, if it actually solves the problem, if it has any issues large or small, etc.

Yes, this is exactly how I am feeling. There is no way for me to actually deeply understand the problem and solution spaces if I am not in it. And you have to be in it to see all the details and possibilities. Without it, they are way too broad and you will never be able to define them detailed enough in a single or even multiple prompts to an agent. 


## Structured Systems

> For Juniors this is greatly raising their skill floor, as opposed to a senior where at best it's doing something they already can do, just faster. The elephant in the room being that if you aren't senior enough to have written the code you'll probably run into a catastrophic bug that you are incapable of fixing (or prompting the LLM to fix) very very quickly. Really it's just the next iteration of no-code hype where people dream of building apps without code, but then reality always come back to the fact that the essential skill of programmers is to understand and design highly structured and rigid logical systems. Code is just a means of specification. LLMs make it easier to leverage code patterns that have been written over and over by the hundreds of thousands of programmers that have contributed to its training corpus, but they can not replace the precision of thought needed to make a hand-wavy idea into a concrete system that actually behaves in a way that humans find useful.

I can relate with this comment above so much. When I don't have a clear plan in my mind and a clear mental model of the system I am trying to build, all [[Claude Code]] prompts just lead to a big old mess. This is going to be a skill that's really needed. Understanding how to create "structure" and "systems". And even better, understanding how to make them easy to use for other programmers (and today agents).

## On Juniors

> Senior devs earned their experience of what is good/bad through **writing code**, understanding how hard and annoying it is to make a change, then **reworking those parts or making them better** the next time. The **feedback loop** was impactful because it was based on that code and them working with that code, so they knew exactly what the annoying parts are. Vibe-coding juniors do not know that, their conversation context knows that. Once things get buggy and changes are hard, they will fill up their context with tries/retries until it works, leading to their feedback loop being trained on prompts and coding tools, not code itself. Even if they read the outputted code, they have no experience using it so they are not aware of the issues - i.e. something would be better being a typed state, but they don't really use it so they will not care, as they do not have to handle the edge cases, **they will not understand the DX from an IDE**, they will not build a full [[Mental Model]] of how it works, just a shallow one. This leads to insane inefficiencies - wasting 50 prompt cycles instead of 10, not understanding cross-codebase patterns, lack of learning transfer from codebase to codebase, etc. With a minor understanding of state modeling and architecture, an vibe-coding junior can be made 100x more efficient, but **due to the vibe-coding itself, they will probably never learn state modeling and architecture, learn to refactor or properly manipulate abstractions**, leading to an eternal cycle of LLM-driven sloppypasta code, trained on millions of terrible github repositories, old outdated API's and stack overflow answers.
> "They will fill up their context with tries/retries until it works" Or until it does not. On numerous occasions I've observed LLMs get stuck in the endless loop of fix: one thing, break the other. Senior is capable of fixing it themselves and juniors may not even have a clue how the code works.

(bold parts highlighted by me)

> The worst possible situation is to have a non-programmer vibe code a large project that they intend to maintain. This would be the equivalent of giving a credit card to a child without first explaining the concept of debt.

## The craft of coding 

> I treat my coding as a craft. That has become much easier, since retiring. I'm quite aware that doing things my way isn't commercially viable, but no one pays me to do it. I do it for myself. That said, I find that it's important to always be challenging myself.

## Understanding the concepts of a system

> There is the appealing idea that AI-assisted programming means better tools which lets us build more ambitious software. That is certainly true at the level of the individual and without doubt a developer with an agent will be dramatically more capable of changing a codebase. But **large software projects have never been limited only by how quickly an individual can produce code**. They are **limited by how well people can coordinate their understanding of the system they are changing**.
> 
> The shared language of a software project is not English or Python but it is the **common understanding** of what its **concepts** mean, where the **boundaries** are, which **invariants** matter, who **owns** what, and why the system has the **shape** it does. This language is rarely written down in one place. It lives partly in documentation and code, but also in code review, conversations, arguments, and the experience of having to explain a change to somebody else.
> 
> Before agents, some of this shared understanding was maintained by friction. If I wanted to change your storage layer, I usually had to read your code, ask you questions, and perhaps coordinate with another team whose service depended on it. This was slow, and much of that slowness was waste but not all of it was. Some of it was the process by which your understanding became mine, and by which both of us discovered whether we still agreed about how the system worked. This friction synchronizes people.
> 
> Agents remove much of that friction. I can ask an agent to add OAuth, you can ask one to add caching, and somebody else can ask one to rebuild the database from first principles and make the UI pink. Each change can be reasonable in isolation. The code can compile, the tests can pass, and the explanations can be generated on demand. None of us necessarily has to talk to the others, or even acquire the part of the shared model that the change once would have forced us to learn.
> 
> As I said many times before: agents do not feel pain, only humans do. Agents now let us act in parts of the system where we would previously have needed other people and in code bases where the people would have revolted.

https://lucumr.pocoo.org/2026/7/13/the-tower-keeps-rising/

