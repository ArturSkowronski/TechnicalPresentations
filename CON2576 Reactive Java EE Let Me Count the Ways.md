##CON2576 Reactive Java EE Let Me Count the Ways!
* Reactive is vague term
* Reactivity is natural in Event driven systems
* Reactive was always important technique, but it wil be more important in Internet of things
	* People are slow (easier to be responsive), machines are fast
* Reactive programming is not a silver bullet
	* it's harder to write Event Driven Software
	* horizontal scalability can be cheaper
* JMS MDB
	* Asynchronous session beans
		* @Stateless -> @Asynchronous 
		* Just annotation on a POJO
		* High throughput
		* Not persistent
		* Not fault/error tolerant
* CDI Events/Observers
	* Observer patter via DI Framework
* Asynchronous Servlets
	* greater utilization of threads
	* AsyncContext
* Asynchronous Servlet NIO
	* WriteListeners & ServletOutputStream
		* OnWritePossible & OnError
* ManagedExecutorService