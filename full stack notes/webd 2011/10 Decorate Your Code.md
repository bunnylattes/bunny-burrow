---
class:  web 2011
module:  module eight
date:  2022-07-17
tags:  #objectoriented #web-2011
---

# Decorate Your Code

### Design Issues

#### Interfaces
- An interface defines the methods an object must have in order to be considered a particular type
- Interface is an abstract type that specifies behaviour that classes must implement
- Interfaces allow different classes to share similarities
- Not all classes need to have the same behaviour
- Doesn't allow for runtime changes in behaviours
- Becomes a maintenance nightmare

### The Strategy Pattern

#### Program to an Interface, Not an Implementation
- Clients remain unaware of the specific types of objects they use, as long as the objects adhere to the interface that clients expect
- An **Interface** is essentially a **Supertype**
- Programming to an Interface is basically taking a behaviour that could vary, making it an Interface and creating the varied behaviours
	- Ex: QuackBehaviour as an Implementation is too difficult because some ducks don't quack but squeak. By making the QuackBehaviour an Interface and then creating Concrete Classes for each type of QuackBehaviour, we eliminate that problem.
	- ![[interfaceguy.jpg]]

*The Strategy Pattern* defines a family of algorithms, encapsulates each one, and makes them interchangeable. This lets the algorithm vary independently from clients that use it.

#### The Open/Closed Principle
- Classes should be open for extension but closed for modification
- We know that we must modify existing code for the future, but we do not want to touch existing code because we could create new bugs
- We want classes to be open to extensions of behaviour

### The Decorator Pattern

*The Decorator Pattern* attaches additional responsibilities to an object dynamically. Decorators provide a flexible alternative to subclassing for extending functionality.

- The Components and the Decorators are the most important parts of the pattern
- Component is an Interface/Abstract class
- Decorator class is an Abstract class that implements the Component and there will be concrete classes for the Decorator Abstract class
![[decoratordiagram.jpg]]
- Coding for Beverage Class:
	- *public abstract class Beverage {
			String description = "Unknown Beverage";
			public String getDescription(){
				return description;
			}
			public abstract double cost();
		}*

- Extending the Beverage Class:
	- *public class DarkRost extends Beverage{
		  public DarkRoast(){
			  description = "Dark Roast Coffee";
			}
			public double cost(){
				return .99;
			}
		}*

- It is implementing the Beverage methods here

- Coding for Decorator Class that Inherits from the Beverage Class
	- *public abstract class CondimentDecorator extends Beverage {
		  public abstract String getDescription();
		  }*
- Decorator is Abstract
- Concrete Decorators:
	- *public class Whip extends CondimentDecorator{
		  Beverage beverage;
		  public Whip(Beverage beverage){
			  this.beverage = beverage;
		  public String getDescription(){
			  return beverage.getDescription() + ", Whip";
			  }
		  public double cost(){
			  return beverage.cost() + .10;
			  }
			  }*
- Whip extends CondimentDecorator: we can wrap the condiment around anything!

![[starbuxx.jpg]]