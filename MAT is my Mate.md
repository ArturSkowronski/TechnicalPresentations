MAT is my Mate

* retrieval of memory
	* jmap 
		* com.sun.menagement -> Operations			
		* dumpHeap
	* jconsole
	* jcmd
		* works only as the user who started jvm, not root
* Thread dump = stop the world
* Before dump is full garbage collector
	* You can mark keep unreachable objects
* Shallow heap - Class with primitives without references
* Retrained heap - how much memory we will retrieve if we collect given class
* OQL view 
	* we can make SQL-like queries
* Thread overview
	* Overview of threads
* Leak Suspects
* Top Components
* List objects with ingoing and outgoing references