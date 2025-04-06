Make sure to **always** ask this question.

As a rule of thumb, lower level components shouldn't have to manage their state. Most of the time a bigger component will manage lots of lower level components via its state.
It can then of course push the state to parent components via callbacks when necessary.
