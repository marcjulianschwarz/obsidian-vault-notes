Probably the context provider is not able to reach all the way into the current component. Thus the dispatch function will revert to the default value (which is just an anonymous void function).
