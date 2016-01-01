#CQRS dla każdego - Maciej Aniserowicz

* CQS - jedna metoda nie powinna modyfikować i zwracać danych
* CQRS - podział systemu na Query i Commnady (wykonanie akcji), podział na dwa modele
* Problemy
	* Read
		* Zapytania na modelu domenowym (kopią bazy) przez ORM są bardzo nieoptymalne
		* Repository pattern IS BAD
			* Another complexity
			* don't give option to change db
	* Write
		* Grube kontrolery
		* ... i w domain services
* No CQRS
	* CRUD
	* 1-user domain
		* Blog Draft
* Używać tam gdzie potrzeba, nie dla całego systemu