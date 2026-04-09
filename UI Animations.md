
- 
- subtle scale-down on button presses scale(0.97)
- frequency of use
	- delightful animations only in places that rarely get used
- most hover effects -> no animation 
	- depending on how often they are seen by the user in a day
- keyboard-controlled -> no animation
- fast spinners
- less than 300ms -> preferably less than 180ms
- tooltip short delay, but once shown, no animation
- don't animate from scale(0) but from scale(0.9+)
- use ease-out for things entering or exiting the screen
- transform-origin should be set correctly (center is default and often wrong)
- use `filter: blur()` to smooth out fading animations 

https://animations.dev/

https://emilkowal.ski/ui/7-practical-animation-tips