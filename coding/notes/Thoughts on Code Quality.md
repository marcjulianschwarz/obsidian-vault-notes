
**What to do to prevent bad code:**
1. Develop expertise in at least one area, and use it to block the worst changes and steer people towards at least minimally-sensible technical decisions.
2. You should care about the things you build

The codebase you spend time on at work is the company’s codebase, and they can do whatever they want with it. You should communicate the risks and consequences of decisions, but ultimately it’s not your call.

## My Explicit Guidelines

### Behaviour
- Every manual action \[in the codebase\] must have a dual purpose of completing a task and improving the system.

### Concrete Principles
- Try not to use booleans as state variables. Instead use an enum or union of literals to represent any amount of states. This gives you the flexibility for adding new states and only allows specific states at a time instead of any combination with booleans.
- Code that affects the behavior of something should be easily discoverable from the point its behavior affects 
	- High Cohesion, Low Coupling
	- for example
		- init a variable closer to its usage
		- prevent having wrapper functions -> instead inline code 
		- prevent global mutations
- Splitting along the scope/behavior lines is more understandable than splitting along file types
- Policies instead of Permissions / Flags
- See [[Thoughts on Refactoring]]
- See [[My Coding Principles]]
