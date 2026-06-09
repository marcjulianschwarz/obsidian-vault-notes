

- If your class has a ton of private methods that hide behind only few public methods, it might be an iceberg and should be refactored into more classes that get orchestrated by one class. Each of the smaller classes can be tested via its public API
	- **Increase public API space** over multiple small classes and **Decrease private API space** in few big classes

