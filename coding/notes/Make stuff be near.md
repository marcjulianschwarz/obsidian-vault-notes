Basically make sure that stuff that belongs to each other is also near each other. 

Best example: React. HTML, CSS and JS can all be defined in a single file. That way a button component for example can have everything it needs right at one point. They styling, the general markup and the logic in JS that the button should exhibit.

Another example, I really enjoy naming files in a structured manner. For example for GitHub workflows:
- test-backend-unit
- test-backend-e2e
- test-frontend-unit
- test-frontend-e2e

I am basically taking into account how I will be searching for these files and make sure they are near each other in the file explorer. Let's say I want to run a certain test:
- first I want to find the test files
- then I look for which service to run a test on
- then what specific test

So it makes sense to use that order in the naming scheme.