##AWS re:Invent 2015 | (GAM402) Turbine: A Microservice Approach to Three Billion Game Requests a Day
https://www.youtube.com/watch?v=txJmBA4cdQM

* Game has the most traffic the first day 
* Game studio needs multitenant architecture - many games, many product teams
* They have multiple Amazon Accounts with VPC specific access
* They are using specific adresses for each Machine
* Less RAM memory - faster memory storing in MongoDB
* Throttling - Important to know your definition of real time to tune caching  - Focus on highest impact
* Throttling - Reduce Writes to allow reads.
* Throttling - Block CUstomer impacting calls
* Throttling - 
* EBS can be bootleneck
* Metric Overload - don't show Graphs unless you need them
* Don't make you Metrics clutter
* Contact Vendors before launch
* Don't solve low hanging fruits