###Twitter Flight 2015 - A Deep Dive into the Answers Backend by Ed Solovey
https://www.youtube.com/watch?v=G1LrMXR3Zko

* Using lambda applications
	* Proccess Offline
	* Map Reduce Network
	* Batching
* Simultanous Offline and Realtime processing
* Problem - load per app is not predictable	
* Probabilistic Data Structure
	* Cardinality - Hyper-Log-Log
	* Retention - Bloom Filter
	* Session Duration 
		* Percentile Bucket
		* Split into seconds
		* Like JavaMelody
* Trade off event cannot be splitted equaly, need to be sticky - Hot Spotting
	* HotSpots - box acquiring more traffic than rest
	* Stream sized Grouping
		* Moving traffic between machines 
	* Sampling
		* Procesing just statistically important amount of data
		* Not 10% of events from all devices - 100% of events from 10% devices