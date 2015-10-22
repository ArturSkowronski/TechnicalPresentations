### Smart Hacker Space: Tomek Cejner: Crafting APIs that your users will love


* Model dojrzałości Richardsona - tak się to nazywa ;]
* Design + Implementation
* API First Class Design
* Schema Frist Design
* Step Zero : Know Your Audience - Driver of Design 
	* Small Set of Known Developers
		* More Elasticity
	* Large Set of Unknown Developers
		* Better Suit
* Concerns of Data
	* Gathering (Producer)
	* Formatting (Consumer)
	* Deliver (Consumer)
* Step One : List of all parts - Semantyczne Deskryptory z punktu widzenia klienta
* Step Two : Define State Transitions (Diagram stanów) - hyperlinki
* Step Three : Naming Things - Reuse standards - 
	* Iana link relations
	* Schema.org
	* Microformats
	* Dublin Core
* Step Four : Document Created Arifacts
	* Swagger
	* ApiDoc
	* WSDL
* Backward Compatibility
	* New Fields optional or with defaults
	* Do not rename fields
	* Do not remove fields
* Forward Compatibility
	* Accept Unknown Fields
	* Watch Out for Scalar Values - wrapping values
	* Watch Out for Enums 
* Generated Clients
	* Consistency
	* Eventual Better Than Elegance
	* Generate from documentation + wrzucenie do GIT
* Governance
	* API is a Contract
	* Plan a deprecation
	* Netflix 
		* API Versionless
* Resource Based vs Experience Based API
* CRUD: Baza danych przez internet :D