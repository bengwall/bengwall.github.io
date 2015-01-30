---
published: false
---

- https://kobra.io/#/

Revel.js Presentations
- https://github.com/zachsnow/angularjs-talk
- www.slides.io
- 

Quote and Bind Design
Lessions Learned

Slide 1
- Started with a Service driven design
- Ended up with a Domain driven design

Slide 2
- Application Layers
	- Application/Invocation Layer (Controllers, Directives, Filters)
    - Business Service Layer (Services)
    - Integration Layer (Services)
    - Domain Layer (Services) ***APPEAR***
    
Slide 3
Service Driven
- Started by placing functions in the business services
	- PersonBusinessService
    - QuoteBusinessService
    - VehicleBusinessService
- Controller -> Business Service -> Integration Service

Slide 4
Example #1 - Service Driven - Saving a Vehicle
VehicleController
	- VehicleBusinessService.getVehicle(vehicleId);
VehicleBusinessService
	- VehicleDataService.getVehicle(vehicleId);
VehicleDataService
	- Make rest call and return Response

Slide 5
Example #2 - Service Driven - Getting Persons Full Name
PersonController
	- PersonBusinessService.getFullName(person);
PersonBusinessService
	- return person.firstName + ' ' + person.lastName;
    
Slide 6
Model Driven
- We went from using POJO's to Classes
	- Person
    - Vehicle
    - Quote
    - Address
    - more
    
Slide 7
Example #1 - Model Driven - Saving a Vehicle
VehicleController
	- var vehicle = new Vehicle;
    - vehicle.load(vehicleId);
Vehicle (model)
	- VehicleDataService.getVehicle(vehicleId);
VehicleDataService
	- Make rest call and return Response

Slide 8
Example #2 - Model Driven - Getting Persons Full Name
PersonController
	- person.fullName;
Person
	- return this.firstName + ' " + this.lastName;
    
Slide 9
What's happening here
- Encapsulation
	- The data and methods are contained together in the same object.
    - This allows some pretty cool concepts.
    	- The person knows how to save itself and transform itself.
    	- It is much more intuative to code and structure the logic.
    
    PersonBusinessService.getFullName(person); 	-> person.fullName;
    PersonBusinessSerivce.isDriver(person) 		-> person.isDriver;
    UtilService.formatDate(quote.effectiveDate)	-> quote.effectiveDateFormatted;
        
        
Slide 10
Full Example


Slide 11
Result
- Business services went completely away.  All code fit into models.  Surprise.
- Code became organized much better.  Lines became much more clear.
- Coding is much more intuative and enjoyable.  Being properties and methods on the actual object, devs had a better sense of where to put their code and what to code to put there.

Slide 12
Future
- Javascript is functional, but more OO type constructs in the future.  ...slowly...
- There are alternative frontend languages trying to do this already
	- Dart
    - CoffeeScript
    - TypeScript
	They have different approaches and introduce some cool capabilties.
    