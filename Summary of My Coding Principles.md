---
tags: ["coding","summary"]
---
# Summary of My Coding Principles

## General Principles
* Prefer simplicity over complexity.
* Focus on simple, side-effect-free functions rather than complex objects.
* Increase cohesion by keeping related components together and reduce coupling.

## Function Design
* Ensure clear input and output types, readability, conciseness, and efficiency.
* Short functions with an emphasis on single tasks.

## Refactoring Guidelines
* Apply DRY principles discerningly, avoiding unnecessary atomic refactoring.
* Opt for parameterizing when unsure.

## Abstraction and Structure
* Maintain modular encapsulation and prefer comments to excessive extraction.
* Separate data from actions and use dependency injection and composition over inheritance.
* Embrace immutability and avoid global state changes.

## Git Practices
* Regularly pull and rebase, use consistent feature branch naming, and prefer squash commits.

## TypeScript Preferences
* Favor interfaces over types, use union types over overloads, and minimize type parameters.

## Backwards Compatibility
* Strive for backwards compatibility by making changes additive and progressively migrating deprecated interfaces.
