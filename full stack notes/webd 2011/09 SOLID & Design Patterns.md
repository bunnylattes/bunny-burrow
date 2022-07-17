---
class:  web 2011
module:  module seven
date:  2022-07-17
tags:  #objectoriented #web-2011
---

# Design Patterns

### Design Principles
**Encapsulate What Varies**
- Identify the aspects of your application that vary and separate them from what stays the same
- There are 23 different original patterns
- Design patterns are about reusing and the design experience, design patterns are expressed by:
	- a definition
	- a class diagram
	- collected into a catalog of patterns

### Encapsulate What Varies
- Most foundational principle and is found at work in almost all design patterns
- Identify the aspects of your app that vary and separate them from what stays the same
- Is the same code changing with every new requirement? then it must be encapsulated
- This way you can change it without affecting parts that don't vary
	- **Simple Factory Pattern:** We can bring the varying code into its own class and have its own method, now it can be altered at any time without affecting the rest of the code
- Always look for code that changes
- Alter or extend the code that varies without affecting code
- Basis of almost every design pattern
- Pay attention to how each pattern makes use of this principle

### Favour Composition Over Inheritance
- *Has a* is better than *is a*
- Identify the aspects of your application that vary and separate them from what stays the same
- *Is a* is an **Inheritance Relationship**
	- Dog *is a* animal
	- Taxi *is a* automobile
- *Has a* is a **Composition Relationship**
- Dog *has a* owner

**Coffee Example**
- Inheritance: Varying types of Coffee are children of the Coffee class
	- This leads to neverending classes and is not well maintained (the cost override makes maintaining it difficult with varying cost)
- Composition: Using a Coffee *has a* condiment is much cleaner and easier to maintain
	- We create a condiment class
	- Have the coffee be composed with 0 or more condiments (an array)
	- Now we just instantiate a coffee with the condiments
- Composition Benefits
	- We can add any number of condiments easily at runtime
	- Implementing new condiments by adding a new class
	- No code duplication
	- Avoid class explosion
	- Instead of inheriting behaviour, we can compose our objects with new behaviours
	- Allows behaviour changes at runtime, not composition

### Loose Coupling
- Strive for loosely coupled designs
- Components should be independent, relying on knowledge of other components as little as possible
- Tightly coupled classes occur when changes to one affect the other
- Loosely coupled should be able to be changed independently
- Naturally reduces dependency between components; systems can handle change well

### Program to Interfaces, Not Implementations
- Where possible, components should use abstract classes or interfaces instead of a specific implementation
- "Program to a super type"
- Making an abstract class with two concrete subclasses and having the system connected to the abstract class, we can use any concrete subclasses of the abstract class
![[killerweb.jpg]]
- No code changes are needed as we add new types of databases, this makes it more maintainable
- The new operator only works on concrete types
![[pizza.jpg]]
![[pizzare.jpg]]

**Program to Interfaces**
- Use interfaces or abstract classes when possible, rather than concrete classes
- Allows you to better exploit polymorphism
- Frees classes from knowledge of concrete types
- Improves extensibility and maintainability

### Single Responsibility Principle
- A class should have only one reason to change
- Separate out responsibilities with different interfaces with single responsibilities
- Look at change in your class: are parts of it changing while other parts arent?
	- If not, there's no reason to refactor the design
- Change only matters if it really happens, if things aren't changing in the code then it doesn't need to be fixed
- Apply Single Responsibility when the need is real or else it's just being complex

### Open/Closed Principle
- Our object-oriented designs should be open for extension, but closed for modification
- Composition over Inheritance! Make behaviour classes
- Allows new behaviour without risking changes to proven code
- Improve maintainability and extensibility of a design

### Liskov's Substitution Principle
- You should always be able to substitute subtypes for their base class
- Don't assume an is a relationship adheres to hierarchy

### Interface Segregation Principle
- Classes should not be forced to depend on methods that they don't use
- Disadvantages of a polluted interface
	- When you continue to add new methods to an interfact that are not relevant for every interface
- **Cohesion**
	- How strong are the relationships between an interface's methods
	- Do they use all the methods of the class? It has high cohesion
![[segregate.jpg]]

### Dependency Inversion Principle
- High level modules should not depend on low level modules
- Both should depend on abstraction and the abstraction should not depend on details
- The high level policy is the abstraction that underlies the design
![[abstraction.jpg]]
- Instead of having the RemoteControl class directly rely on the Television class, we create an OnOffDevice abstraction so the RemoteControl can turn on and off many different types of devices, not just the Television
- Frees our high level compoinents from being dependent on the details of low level components
- Helps design software that is reusable and resilient to change
- All relationships should involve abstract classes of interfaces
- Abstractions allow details to remain isolated from each other