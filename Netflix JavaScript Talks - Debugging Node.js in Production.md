##Netflix JavaScript Talks - Debugging Node.js in Production

* Applying scientifical method
* CPU is Critical
	* Node is essentially single threaded
	* One slow request lock all other
* Using linux perf event
	* don't show JS stacktraces, just V8 stacktrace
* node --perf_basic_prof_only_functions
	* outputs the files in a format that can be readed by standard perf tools
	* availble in node v5
* problem - too many stacktraces
* Solution - Flame Graphs
	* x-axis - percent of time on CPU
	* y-axis - stack depth
	* brendangregg/FlameGraph
* there are lodash functions that are slow on node.js
* Dramatically reduce request latency
* Performance Technique
	* Sample stack traces via perf(1)
	* Visualize code distribution
	* Identify candidate code paths performance improvement
	* Repeat
* Runtime crashes
	* Postmortem debuging
		* Load core dump
		* Debug
		* Engineer Fix
	* node --abort_on_uncaught_exception throw.js
	* tools to analyze stack
		* lldb-v8
		* llnod
		* mdb_v8 - for solaris
* Memory Leaks
	* Local specialist ;) Reed Hastings
	* Generate Core Dump Ad-hoc
		* look on objects that are suspicious
		* compare with successful core dumps and compare
			* objects delta
		* find root object 	