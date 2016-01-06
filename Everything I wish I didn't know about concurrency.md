#Everything I wish I didn't know about concurrency
https://www.youtube.com/watch?v=RR62KqHEVfM&list=WL&index=3

* Processes - many operating systems adress spaces scheduled on given cpus
* Thread - many Subprocess using single adress spaces scheduled on given cpus
* Distributed Systems - Many machines without shared resources

* Ways of process communicate
	* Channels
		* Two ends communication between two process
		* Can be synchronous or Aynchronous
		* Sockets, Go channels, Akka, Erlang
		* Actor model is special case
	* Brodcast
		* Very common in network/hardware
		* Single sender many receivers
		* Not that useful in software
	* Shared State
		* Both have access to the same memory/database
		* I can write something, somebody can read it
		* Java Memory Model
			* How do threads interact with memory
			* Compilers can reorder statements
			* Specification is unclear for reordering
		* C++ 11 MM tried to be tested formaly, failed miserably
* Solutions for Race Conditions
	* Mutex - mutual exclusion - pessimistic locking
		* Critical section - section in lock
		* java synchronize word is big lock on the object-level - on every usage of objects
	* Reader-Writer Locks
		* When we want read there is no problem
		* When we want write, we need wait for all readers to leave critical sessions
		* Readers can potentially block writes indefinitely
		* Fairness can be write-optimized or read-optimized
	* Atomic Compare and Swap
		* implemented on hardware
		* before you write a value, check if value is the same that one when you started write
	* When contention is rare, you don't need locks
		* Optimistic concurrency control
			* If fail, retry - like in DB
* Correctness
	* Safety - nothing bad happend
		* Doing nothing is always safe
	* Liveness - Something good eventually happens
		* you will have access in future
* Deadlocks
 	* If error, locks must be released
* Starvation 
	* nobody can acquire lock
	* causes
		* Readers-Writer locks
		* "Phase issues"
		* Asymetric workload 
* Live Locks
	* click switch machine
	* You change env, it changes back
	* Two locks which respond to each other simultanously
	* two click switch machines
* How to don't get pitfalls
	* Idempotence
		* f(f(x)) = f(x)
		* great for optimistic concurrency
	* Commumativity
		* x * y = y * x
		* Parallesiation is example
	* Immutability
		* Stop changing
		* no scenarios write after read, read after ride
	* Producer Consumer
		* Single producer
		* Mutex in queue
		* many consumers
	* Fork join
		* fork work
		* do it independly
		* join
	* Java 8 Splitterator
		* split work on pull of threads
		* good for divide and conquer
	* Map/Reduce
		* split work and do in part
	* Shared nothing
* Comprehension is the greates barrier to building correct concurrent systems
* Concurrent systems are nearly impossible to tests
* "Beinf careful" is not suffcient. Good abstraciton is most important
