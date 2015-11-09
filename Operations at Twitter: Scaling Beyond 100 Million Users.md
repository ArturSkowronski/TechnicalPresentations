#Operations at Twitter: Scaling Beyond 100 Million Users
https://www.youtube.com/watch?v=z8LU0Cj6BOU&list=WL&index=5

* 2010 year
* Web API - 25%, API 75%
* Unix friends fail at scale
	* CRON
	* Syslog
	* RRD
* Operations Mantra
	* Find weakest point
		* Metrics + Logs + Science = Analysis
	* Take corrective action
	* Go to next weakness point
	* Mean time to detec (MTTD)
	* Mean time to Recover (MTTR)
* Think of System Management as programming task
	* The faster the better
	* Puppet
* Profilingg
	* Networ Services
		* tcpdump + tcpdstat, yconalyzer
	* Introspect with Google prftools
* Darkmode
	* Feature flags
* Unicorn better than Apache
* Rails
	* Problem with caching
	* memory leaks
* Memcache
	* Network memory isn't infinite
* Cache
	* Cache with long TTL (60s)
	* Don't cahce everythinh
	* Invalidation is hard
* MySQL
	* Replication Delay
		* Multiple masters
		* Reading from master - slow sead
	* Social Network is not good for RDBMS
	* FlockDB is better
* Database is not the best store
* Instrument everything
* Use metrics to make decisions
* Don't make dependencies between services
* Be Async
