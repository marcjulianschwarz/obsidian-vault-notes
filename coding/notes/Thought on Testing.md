First things first: I LOVE TESTING. 


- Being indirectly accessible through the public API != being part of the public API.
- If your private function is not testable through the public API, then perhaps it's a dead code and should be removed? 
	- Your class is indeed an iceberg (reason 1) and should be refactored.
		- [[Thoughts on Refactoring]]


@RobertHarvey if you can’t test a private function through a public API then delete it as it serves no useful purpose. – 
David Arno
Commented Oct 21, 2018 at 18:21