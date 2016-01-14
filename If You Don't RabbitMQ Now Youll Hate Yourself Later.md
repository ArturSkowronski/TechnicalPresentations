#If You Don't RabbitMQ Now You'll Hate Yourself Later

* JMS + Hornet
	* Event works just in one service
	* Cannot scale Consumers and Publishers independly
* RabbitMQ for the go
* Rabbit per module
* NodeJS can consume modules
* Why Rabbit
	* Not beeing a prisoner of given role
	* Offload JBoss Services
	* Lots of clients for alle technologies
	* 1m records per second in Google
* Basic Concepts
	* Exchange
		* Joiner beetwen publisher and subscriber
		* Decides where message will be routed
		* Has four types
			* Routing algorithms
			* Types
				* Fanout - broadcast message to all subscribers
				* Topic
					* Dynamic choose of messages
					* Like JBoss Selectors
					* Can use wildcards
				* Direct
					* Easier Topic
					* Using Exact Match Filtering 
				* Header
					* Routing is complicated
					* Hard to be expressed as binding key
	* Message queue 
		* named entity holding messages and forward to applications
		* Is joined to exchange by binding
	* Binding 
		* filter changes which should be passed
	* Binding Key
* tryrabbitmq.com
