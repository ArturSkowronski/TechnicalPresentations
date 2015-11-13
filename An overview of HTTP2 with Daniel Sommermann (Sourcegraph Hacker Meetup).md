#An overview of HTTP/2 with Daniel Sommermann (Sourcegraph Hacker Meetup)
https://www.youtube.com/watch?v=-yxQIRl6Qic&list=WL&index=4

* Motivations
	* Handshake roundtrip is pretty big
	* Expensive creating new connections
	* Congestion Avoidance - reuse connections, don't use new connections
* Many redundant information - due to stateless structrue they are repeated
* HTTP/2 and SPDY are binary
* TLS everywhere
* HTTPS is HTTP over TLS
* HTTP2 is in the same layer as SSL  - Session Layer
* Pipeline problems
	* Not every request has the same processing costs
	* Multiplexing is soultion
	* You can acquire resources dynamically
* SPDY/2 DOS Problem
* SPDY/3 Flow
* SPDY/3 also has DOS Problem
* SPDY/3.1 Flow
* SPDY in Facebook
	* Proxygen - https://code.facebook.com/posts/1503205539947302
	* 80% gain over HTTPS
	* 66% gain over HTTP 
	* 200 ms gain request
* Hpack - compression for SPDY
* HTTP/2 Priorities support
	* Additional complexity
	* Grouping
* Server Push

