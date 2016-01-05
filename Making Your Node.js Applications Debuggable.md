#Making Your Node.js Applications Debuggable

 * Profiling
	* Performance - amount of processor used
	* Memory - amount of memory used
* V8 CPU Profiler
	* trigger profiler on / off - capturing information
	* V8 will capture stack and frame trace in given intervals
	* self time - time to run the function, not including any function that is called
	* total time - time to run the function, including any function that is called
	* FlameGraph from N|Solid
	* Sunburst from N|Solid (Circular FlameGraph)
	* TreeMap from N|Solid
	* tools
		* npm v8-profgilers
		* npm node-inspector
		* StrongLoop arc
		* NodeSource N|Solid
* V8 heap snapshots
	* JSON file describing every reacbli JS Object in app
	* 2x heap shanpshot
	* grouped by
		* shallow size - the size of memeory held by an object itself
		* retained size - amount of memory that will be restored after GC
	* tools
		* heapmap
			* can do diff shapshots
* Profiling tips
	* look for width in trace visualizations
	* script profiling a web server
	* use node/v8 option --no-use-inlining - stack will have more info