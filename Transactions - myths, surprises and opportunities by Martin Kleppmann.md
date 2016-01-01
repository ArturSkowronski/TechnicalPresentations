##Transactions: myths, surprises and opportunities by Martin Kleppmann
* NoSQL = NoTransaction
* ACID = More mnemonic or precise
* Durability
	* you log your transaction to the archive tape. If your disk fail you just repeate transition
	* fsync to disk
	* replication
* Consistency
	* tossed in to make the acronym work
	* different than in acid
	* Transaction move DB from one consistient state to another
* Atomicity
	* NOT ABOUT CONCURRENCY
	* If something is wrong, transaction is rollbacke 
	* All or nothing
	* Transaction - multiobject atomicity
	* Abortability in truth
* Isolation
	* Serializable
	* Each transaction behaves as if everything inside was created lineary
	* Isolation Levels
		* Serializable
			* It was slooow after first implementation
			* In oracle it means Snapshot Isolation
			* Prevent Write Skew - if premise of decision is no longer true
			* Solution
				* Lock everything you read - two phases lock
					* Read entire DB = stops all writes
				* H-Store
					* VoltDB, Datomic, Postgre
					* Literally serial order - orderize transactions (if they are very fast)
					* Keep everything in memory
					* Locality of data and computing
				* Serializable Snapshot Isolation 
					* Detect conflict and abort
					* Lock like in 2PL but locks don't block, just gather information
					* abort if conflict
					* Optimistic - assume there is not many conflicts
		* Repeatable Read
			* In MS SQL Server
			* Prevent Read Skew
		* Snapshot Isolation
			* Postgres, mySQL,SQL Server (with SNAPSHOT)
			* Prevent Read Skew
		* Read Commited
			* Can be done without global coordination
			* Read Skew can happen
			* Prevents Dirty Reads - cannot read data that are not commited
			* Prevents Dirty Writes - order of writes
		* Read Uncommited
	* Hard to understand - they are implementation details
	* They work in singleinstance systems
* Transaction in microservices
	* Database per microservice
	* Transaction boundary - just in one service
		* Compensating transactions
		* If something fails in different place, request for rollback - A
		* Integrity constrains - if problem happen - apology client ;) - C
		* After the fact, rather not preventing them
	* We don't want distributed transactions
		* Atomic broadcast problem
		* Total ordering - consensus
	* Causal relationship - we don't know how one service influence another
	* At beginning - pure eventual consisency
	* Then - Casuality - we want to hae order of some information - can be made without global coordination
* Transaction in stream processing
* Every sufficient large deployment of microservices contains ad-hoc, imfromally specific bug-ridden, slow implementation of half of transactions