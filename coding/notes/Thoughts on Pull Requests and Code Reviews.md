
## Guidelines

- Prefer smaller self-contained PRs over larger PRs touching many parts of the codebase at once
	- sort of max 500 lines, better less
	- when it makes sense
- A PR should do a single thing
	- if necessary, do multiple things in clear cut commits and mention this in the PR description 
- PR titles should at least include ([see Linux kernel](https://www.kernel.org/doc/html/v7.0/process/submitting-patches.html#the-canonical-patch-format))
	- some ticket number
	- system/subsystem it touches
	- short summary of change

## LLM Generated Code

- unnecessary comments
- emojis in comments and debug logs 
- duplicated code
- not honoring naming conventions 
- extremely defensive written code 
	- trying to catch all and random exceptions
	- does it swallow errors
	- doing retries everywhere
	- catching edge cases that can't even happen
	- logging everything
- having "fallbacks"
	- LLMs like to generate fallback routes for everything instead of fixing the underlying problem or abstraction

If I'm reviewing a PR and when I ask why code is doing something and the response is "because the Al suggested it" I'm probably rejecting it. You need to understand what the code is doing. Remember, it's Copilot, not the captain.


## Code Style

Someone who can't bother looking around and adapt their style to the surrounding code sounds like a problem to me. Even more than that, it means the developer has spent no time understanding the surrounding code, and thus is likely adding debt/CRUFT/risk.

## Self-Review

- let me catch things I usually can't find
- adding additional comments to parts that might need clarification for the reviewer


## PR Descriptions

Minimally, I would like **context** for the change, **why** it required a change to this part of the codebase, and the **thought process** behind the change.

## Code Review

### how to review 

- treat as high priority 
- start immediately and take your time 
- the absolute maximum turnaround on a review round should be one business day
- start high level (refactors, architecture, etc.) and work your way down during review rounds to lower level changes (variable naming, file naming, style issues, etc.)
- be generous with code examples 
- "we", passive voice, questions -> frame your notes as requests instead of commands
- tie notes to principles, not opinions -> always give reasons for suggested changes 
- repeated patterns should only be called out once 

### after review

- unclear parts / question answered in the PR discussion should result in code changes or comments added



## Temporary vs. Permanent Authority 

## Resources

- https://mtlynch.io/human-code-reviews-1/
- https://mtlynch.io/human-code-reviews-2/
- https://www.chiark.greenend.org.uk/~sgtatham/quasiblog/code-review-antipatterns/
- https://mtlynch.io/code-review-love/