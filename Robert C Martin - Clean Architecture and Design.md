Robert C Martin - Clean Architecture and Design

* Two kinds of business rule
	* Interactor (Control object, Use Case) - Particular to given application
		* Part of applicatin model
		* Has execute method
		* Communicate Back forth with user
		* Tells entity what to do 
		* Have boundaries (Java interfaces)
	* Entities/Bussines Object - Rule that trancende the application
		* Part of domain model
		* Business rules application agnostic
* We have interface keyword in java cause we don't like multiple inhertinance
	* It's hard to do it in compiler and they were lazy
* Request model is Data Structure
* Model View Presenter
* Reason to have DB is historical - after the hard drive.
* A good architecture maximize amount of decision you can make later