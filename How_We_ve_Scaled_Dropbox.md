#How We've Scaled Dropbox
https://www.youtube.com/watch?v=PE4gwstWhmc&index=5&list=WL

* Dropbox Challenges
* Write Volume
* Read to write in Twitter: 1000:1
* Read to write in Dropbox: 1:1
* Multi petabyte cache
* Dropbox need to be ACID
	* Atomicity - don't have half a file
	* Isolation - you can do offline operation
* HighLevel Architecture
	* Mid 2007
		* Single server
		* 2 People
		* No Users
		* All on single disk
		* Wanted to confirm hypothesis
	* Late 2007
		* Introduction of Amazon S3
		* 3 People
		* Self hosted machine
		* MySQL
		* 0 users
	* Early 2008
		* 50k Users
		* Split syncro and main server
			* Metaserver
				* direct calls to db
				* logic of db calling
			* Blockservers
				* direct calls to db
			* No Servers
		* One DB
		* Don't overbuild
	* Late 2008
		* 100k Users
		* 9 Employee
		* Memcache
		* LoadBallancer
	* Late 2012
		* 100 Employee
		* 50 M users
		* Architecture rather stays the same
		* It's hard to just add servers, even for memcache - hard for consistency
		* Problem with Pythons and Global Interpretation lock - one request time
		* Every LB has backuo
		* Scalling DB hard to do
	* They use log in SQL Db
		
