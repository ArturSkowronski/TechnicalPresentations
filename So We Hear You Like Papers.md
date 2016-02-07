#So We Hear You Like Papers
* Eventual Consistency
	* When we talk about EC, We talk about High Availibility
	* Detection Mutual Inconsistency in Distributed Systems (1983)
		* Origin Points
		* Version Vectors
		* There are not always conflicts, we need to
		* Key Points
			* We need Availibility
			* Gives use a mechanism for efficient conflict detection
			* Teach us that network are not reliable
	* Managing Update Conflicts in Bayou, a Weekly connected Replica Storaged System
		* System designed for weak connectivity
		* EC depndency checks and merge procedures
		* Epidemic algorithms to replica state
		* Application must be aware of integrity involved in conflict detection and resolution
	* CRDTS - Consistency Without Concurrency Control
		* Applying rollbacks is hard
		* Restrict operation space to get provably convergent system
		* Active Area of Research
	* Feral Concurrency Control
		* 67 OS ROR
		* Unsafe > 13%
			* uniq and FK constrains violated
		* Concurrency Control is hard
		* Availibility is important
		* Home-rolling your own concurrency control or consensus algorithms are really hard and difficult to do correctly 
* System verification
	* Verification != testing
	* Mindset
		* Formal Methods
			* Human Assisted Proofs
			* Model Checking
			* Lightweight FM
			* Hight Investement -> High Reward
			* Used in safety-critical domains
			* Used in small/simplified version of a system
		* Testing 
			* Top Down
			* Bottom Up 
			* White Black Box
			* Sacrifice Rigor for something more resonable
	* Verification
		* Safety
			* Nothing bad will happen
		* Lifeness
			* Something good eventualy happend
			* Much harder to verify
	* Leslie Lamport - The specification Language TLA+
		* TLA - Combination of temporal logic with logic of actions
			* Predicate Liveness
		* TLA+ - TLA for Distributed systems with more tracing
	* Use of Formal Methods at Amazon Web Services
		* TLA+ at Amazon
		* Specification
		* Real Usecase
		* Bug they found using FM
		* Use FM specification to teach new engineers
	* Simple testing can prevent most critical failures
		* Majority of errors require just 3 nodes
		* 74% of errors are deterministic
		* 77% failres can be unit tested
	* Molly Verifier
		* Reasons Backward
		* Only Inject the failures it can prove might affect and outcom
		* Middle ground between pragmatism and formalism
	* IronFleet: Proving Practical Distributed Sustems Correct


