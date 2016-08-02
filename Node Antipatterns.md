# Node Antipatterns

* CallBack Hell
  * More memory pressure - more stack and harded to GC
  * Problem with error handling
  * Solution
    * Return early
    * Name your function
    * Don't worry about hoisting
* Using a long list of arguments instead of options
* Abusing variable arguments
* Poor use of modularity
* Overuse of classes for modeling
* Ignoring callback errors
* The Kitchen-Sink Module
  * Unrelated utility functions
  * Should use SRP
* Placing values in global objects
  * Leverage Module Cache
  * Exception - testing frameworks
* Synchronous Execution after initialisation
  * Use synchronous just during initialisation
    * before server is listening
* Dangling source stream
  * Node don't close source stream if closed one is closed
  * pump package
* Changing the way require works
  * Setting NODE_PATH is possible but you shouldn't
  * Every folder should be bounded context
* Monolithic Application
* Little or no automated test
* Testing at wrong level
* Depending on global installed modules
  * folder bin is add to all dependencies
* Using gulp or grunt instead npm scripts
* not measuring code coverage
* Poor use of npm
  * https://libraries.io/
  * http://snyk.io
  * http://nodesecuirity.io
* Performing CPU-Heavy Work
* Unlimited asynchronous iterations
* Large denormalised documents
  * Use streaming
* Use opportunity of use streams
  * Response time bubbles
  * High memory consumption
