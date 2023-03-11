---
class:  web 2011
module:  module ten
date:  2022-07-21
tags:  #objectoriented #web-2011
---

# Creational Patterns

### Types
- Factory Method
- Abstract Factory
- Builder
- Prototype
- Singleton

##### Factory Method
- Encapsulates knowledge about which concrete classes a client uses
	- The client only deals with interfaces

##### Abstract Factory
- Hides how instances are created and put together

##### Builder
- Abstracts the object creation process and allows configuration of new instances
- Allow client to build a complex object in steps and configure

##### Prototype
- Abstracts the object creation process and allows runtime configuration
- Create a new object by copying the existing object and modifying it
- Easier for complex objects

##### Singleton
- Ensures there's one and only one instance created so we can control access to a resource

**Abstracting from concrete types (so client can only rely on the abstract/interface classes) is a common and useful technique to make our designs more flexible and prevent complexity from being spread around in the system. Adding new types and new behaviours is easier in this way.**

###### Priciples are for low level of how we put objects together, patterns are for larger problems.

### Factory Patterns
- encapsulate details of which concrete classes are instantiated
- Client depends only on abstraction
- Can change concrete types later without changing client code

##### Concrete Implementation
- We can use an interface as a type of variable but ultimately we need to create a concrete code

#### A Simple Factory
- Move the code responsible for making a product out of the main code and into a separate factory objects
	- if statements that instantiate new objects move with it
- Code becomes open for extension but closed for modification because we do not touch the client code
![[simplefactory.jpg]]

#### Factory Method
- *The Factory Method Pattern* defines an interface for creating an object but lets the subclasses decide which class to instantiate. Factory Method lets a class defer instantiation to subclasses. *Creational Category*
![[factorymethod.jpg]]
- Factory subclasses decide which products to make
- Factory class is interface/abstract superclass
- There is also an abstract product superclass but with different concrete products that get created depending on which factory concrete class is chosen
- **When to use:**
	- We cannot anticipate the type of object that we will need to create
		- ex: we don't know what kind of pizza someone is going to order
	- We would like to use subclassing to offer multiple factories to a client for creating objects
	- The factory subclasses determine which kind of concrete object we will get
![[pizzafactory.jpg]]
- We can add new types of concrete factories or concrete pizzas


#### Abstract Factory Pattern
- *Abstract Factory Pattern* provides an interface for creating families of related or dependent objects without specifying their concrete classes. *Creational Category*
- **When to use:**
	- User's role determines the interfaces they will use to interact with the system
	- Determines the family of products the user will see and interact with
	- A system that must be independent of how its products are created and represented
![[abstractfactory.jpg]]
- If we decide the client should be using a different family of products, we switch out which factory the client is using to create the products and the new family of products is created for us
![[forecaster.jpg]]
- If the Client is using the Forecaster factory, when the Client calls createView, the Client will get tht ForecasterView, etc
- Depends only on the view and functions abstractions
- Easy to change user role
- Decouple our code from the actual factory
- We can implement a variety of factories
- *Loosely coupled design, encapsulate what varies, relies on abstraction*


### Builder Pattern
- Concerned with encapsulating the complexities of how we build an object
- *Builder Pattern* separates the construction of a complex object from its representation so that the same construction process can create different representations. *Creational Category*
- Want to allow Client to create different representations of the same object
- **When to use:**
	- Want to create objects of the same kind, for example a car
	- The client should have flexibility in how we create the cars (choose options for the car)
	- The process of building a car is independent of the parts that make up the car and how they are assembled
		- If we want a moon roof on the car, it's still up to the car where to put it
![[builder.jpg]]
- Director uses the Builder interfact to assemble the product it has constructed
- Once the director has called the methods to build the product, the Director needs to get a reference to the finished product
- The build method takes all the parts that have been added to the project and assembles the final product before returning to the Director
![[buildcar.jpg]]
- Builder encapsulates the code to construct and represent a car
- Builder API must be general enough to support variations in the concrete builders and products they create
- Builder lets us vary a product's internal representation, Director does not worry about the complexity of the building
- The details of the complexity of construction is what varies so it is encapsulated
- Gives fine control over construction but hides the complexity of assembly
- Open for extension by supporting a variety of concrete builders
- Decoupled build complexity from the client


### Prototype Pattern
- *Prototype Pattern* specifies the kinds of objects to create using a prorotypical instance and create new objects by copying this prototype. *Creational Category*
- This pattern uses cloning to create objects
- A prototypical instance is a prototype we have created to copy and make new instances of itself
- **When to use:** 
	- When we copy an existing object, we get the complex set up for free
	- Don't need to know the concrete class of the object we're creating
	- The client is independent of how an object is created and represented
- *Programming to the interface, not the implementation*
![[prototype.jpg]]
- No need for parallel hierarchy because the type of instance is determined what type is cloned
- Helpful when creating objects that are complex or expensive
- May be more efficient this way
- **Benefits:**
	- Separating the client from the details of creation
	- Encapsulates object creation inside a prototypical instance object
	- Client depends on the prototype abstraction/interfact and not the concrete types of the objects created from the prototype, or the details of how new objects of that type are created
	- Java's Cloneable interface allows bjects to clone themselves with the clone method
	- JavaScript Object.create() and Object.assign() can create and copy objects respectively
		- All objects inherit directly from others in JS


### Singleton Pattern
- *Singleton Pattern* ensures a class only has one instance and provides a global point of access to it. *Creational Category*
- Was likely discovered because of bugs caused by multiple instances when there should have been only one
- **When to use:**
	- We need to ensure only one instance of a class exists
	- Instance must be easily accessible
![[singleton.jpg]]
- Static unique instance will hold the one and only instance
- Private constructor for Singleton so only the Singleton class can call the method
- getInstance returns the instance we have created and it can access and return the static uniqueInstance we created, clients can call this
- *The implementation of Singleton is language dependent and can be tricky to get right*
- Singleton implementation is someone language dependent
- Allows us to control how objects are created, accessed, and used in a system
- Encapsulates the code that is managing a resource
- Change the code in the Singleton if you need to change how the resource is used
- Singleton = single responsibility principle
- Other code in the system that uses the Singleton is tightly coupled to the Singleton