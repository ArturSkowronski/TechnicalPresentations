## Clojure At Scale
https://www.youtube.com/watch?v=av9Xi6CNqq4&index=9&list=WL

* From WalmartLabs
	* Product
		* Digital Recipes 
			* Saving Catcher
			* InstaWatch
		* Data From
			* Redis 
			* Cassandra 
		* One way flow of data
		* Queues
		* 20 Services
* Structuring code
	* Use Components
		* https://github.com/stuartsierra/component
		* To present stateful objects
		* Stateful (with lifecycle)
		* Service (without lifecycle)
		* Composite Component
			* Agrregator  
	* During test don't perform side effects
		* test With Let
		* Don't use mock libraries if you not need them
* Multiple projects are a pain 
* Choosing libraries 
	* check if they don't use too many macros
	* don't enforce specfic code style
	* don't be opinionated to much
	* You need to understand internals
	* Async is good :D
* Logging
	* Don't be scaried to use java libraries 
* Deamonize
	* Commons Deamon


