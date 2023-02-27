# LLD

## Object Oriented Programming
### Class - Entity
	is a user-defined blueprint or prototype from which objects are created.
	Modifiers: 
		A class can be public or have default access (Refer to this for details).
	Class name: 
		The class name should begin with the initial letter capitalized by convention.
	Superclass (if any): 
		The name of the class’s parent (superclass), if any, preceded by the keyword extends. A class can only extend (subclass) one parent.
	Interfaces (if any): 
		A comma-separated list of interfaces implemented by the class, if any, preceded by the keyword implements. A class can implement more than one interface.
	Body: 
		The class body is surrounded by braces, { }.
	
### Object - Instance of a class
	State: 
		It is represented by the attributes of an object. It also reflects the properties of an object.
	Behavior: 
		It is represented by the methods of an object. It also reflects the response of an object to other objects.
	Identity: 
		It is a unique name given to an object that enables it to interact with other objects.
	Method: 
		Functionality
### Access Modifiers
	Defines the access type of the method i.e. from where it can be accessed in your application. In Java, there are 4 types of access specifiers: 
		public: 
			Accessible in all classes in your application.
		protected: 
			Accessible within the package in which it is defined 
			and in its subclass(es) (including subclasses declared outside the package).
		private: 
			Accessible only within the class in which it is defined.
		default (declared/defined without using any modifier): 
			Accessible within the same class 
			and package within which its class is defined.
### Method and Method Passing



## Inheritance
	by which one class is allowed to inherit the features (fields and methods) of another class. 
## Polymorphism
	It refers to the ability of object-oriented programming languages to differentiate between entities with the same name efficiently. 
	This is done by Java with the help of the signature and declaration of these entities. 
	Note: Polymorphism in Java is mainly of 2 types: 

		Overloading
		Overriding 
## Encapsulation
	It is defined as the wrapping up of data and functionality under a single unit.
## Abstraction
	Data Abstraction is the property by virtue of which only the essential details are displayed to the user. 
	The trivial or non-essential units are not displayed to the user. 
	Ex: A car is viewed as a car rather than its individual components.



# SOLID Design Principles

## S - Single Responsibility
	A class should have Single responsibity
	A class should have only 1 reason to change
	
## O - Open Closed Principle
	A class should be open for extension but closed for modification
	
## L - Liskov's Substitution Principle
	An object of a class should be replaceble by an object of its subtype without altering correctness of the program

## I - Interface Segregation
	Clients should not be forced to implement interfaces that they do not use
	
## D - Dependency Inversion
	A class should depend on contract i.e. interface rather than implementation i.e. Class

# Design Patterns

## Creational patterns are ones that create objects, rather than having to instantiate objects directly. This gives the program more flexibility in deciding which objects need to be created for a given case.

	Abstract factory 
		groups object factories that have a common theme.
		Factory of factories
	Builder 
		constructs complex objects by separating construction and representation.
	Factory 
		method creates objects without specifying the exact class to create.
		ShapeFactory
	Prototype 
		creates objects by cloning an existing object.
	Singleton 
		restricts object creation for a class to only one instance.
	
	

## Structural Design patterns concern class and object composition. They use inheritance to compose interfaces and define ways to compose objects to obtain new functionality.

	Adapter 
		allows classes with incompatible interfaces to work together by wrapping its own interface around that of an already existing class.
		Adapter is a structural design pattern that allows objects with incompatible interfaces to collaborate.
	Bridge 
		decouples an abstraction from its implementation so that the two can vary independently.
	Composite 
		composes zero-or-more similar objects so that they can be manipulated as one object.
		Design a file system
		Design a expression evaluator
	Decorator 
		dynamically adds/overrides behavior in an existing method of an object.
		Pizza 
		Christmas Tree decoration
	Facade 
		provides a simplified interface to a large body of code.
	Flyweight 
		reduces the cost of creating and manipulating a large number of similar objects.
	Proxy 
		provides a placeholder for another object to control access, reduce cost, and reduce complexity.

## Behavioral Design Patterns

Chain of responsibility 
	delegates commands to a chain of processing objects.
	Design a logger
	Validation
	Rules Middleware
Command 
	creates objects that encapsulate actions and parameters.
	removing if else if from code
	
	
Interpreter 
	implements a specialized language.
Iterator 
	accesses the elements of an object sequentially without exposing its underlying representation.
Mediator 
	allows loose coupling between classes by being the only class that has detailed knowledge of their methods.
Memento 
	provides the ability to restore an object to its previous state (undo).
Observer 
	is a publish/subscribe pattern, which allows a number of observer objects to see an event.
	Observer Patterns
	Observer is a behavioral design pattern.
    It specifies communication between objects: observable and observers
    
    Example NotifyMe functionality
State 
	allows an object to alter its behavior when its internal state changes.
	ATM System
	Postal delivery system
	AudioPlayer
Strategy 
	allows one of a family of algorithms to be selected on-the-fly at runtime.
	Implemented where a solution can have different strategy/algorithm
	Example
		Google Maps
			Pedestrian
			Bike 
			Car
			
	We can have a strategy for finding best route and each can have its own implementation.
	Which can be configured using based on the selection.
Template 
	method defines the skeleton of an algorithm as an abstract class, allowing its subclasses to provide concrete behavior.
Visitor 
	separates an algorithm from an object structure by moving the hierarchy of methods into one object.



