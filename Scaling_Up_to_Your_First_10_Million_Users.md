##AWS re:Invent 2014 | (SOV204) Scaling Up to Your First 10 Million Users
https://www.youtube.com/watch?v=ccojvcQq858&index=19&list=WL

* Autoscale is a tool, not solution
* Regions are different geographical Zones
* Availibility Zones are totally independent location in regions
* Edges are locations of DNS and CDN
* Vertical scaling downsizes
	* No failover
	* No redundancy
	* Poor separation
	* Cost scales expotentionally
* Database Options
	* SelfHosted
	* Amazon RDS
	* DynamoDB
		* You just define how big throughput you wan
	* Redshift
* Start with SQL DB
	* Mature
	* You don't break SQL with first 10 millions of users
	* You are good with SQL as long as you wan tb generatin 5 GB of data in first year
* NoSQL when:
	* Super low latency
	* Metadata driven app
	* Need Schemalles - not easier, really need
	* Thousand records per s
* More than 100 users
	* ELB
		* Manage itself
		* Heal itself
		* Session Stickness
		* Monitoring
	* App More AZ
	* RDS Multi AZ
* Repeat this way with more instances
* 10k - 100k
	* Move static content to S3 and CloudFront (CDN)
	* Move Sessions and DB Caching to ElastiCache and DynamoDB
	* CloudFront over everything
* Now is time for autoscalling
* MOre than 500k - time for automation
	* Elastic Beanstalk - PAAS
	* OpsWorks - administration tool for Amazon (Puppet, Ansible)
	* DIY - CloudFormation - AWS to Json, able to be versioned
	* Monitoring (CloudWatch)
	* No is time of SOA ^^
* 1m
	* RDS Federation
	* RDS Sharding (Lookup DBs)
	* Time to get rid of RDS
