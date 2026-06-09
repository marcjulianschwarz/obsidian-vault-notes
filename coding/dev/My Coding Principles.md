These are some rules or principles I want to follow for all of my coding projects. Of course they should not be applied blindly but they give a good starting point.



## Git 

- do regular git pulls for the main branch and rebase feature branches on top
- make feature branch naming consistent by linking to an issue number and/or including the ticket type
- prefer squash commits when having lots of unnecessary commits 


## Typescript

- prefer interfaces over types
- Always prefer parameters with union types instead of overloads when possible
- Generics
	- When possible, use the type parameter itself rather than constraining it
	- Always use as few type parameters as possible
	- If a type parameter only appears in one location, strongly reconsider if you actually need it
