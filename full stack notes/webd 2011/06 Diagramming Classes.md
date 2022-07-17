---
class: webd 2011
module:  module three
date:  2022-05-12
tags: term-2 webd2011 
---

# Class Diagrams

## Class Diagrams
**UML Diagrams Controlling Visibility**
- The - sign represents private
- The + sign represents public
- Leave as many Attributes and Behaviours private as possible

#### Converting Class Diagrams into Code
- Diagrams can easily be converted into any language easily
- Symbols and syntax will differ but it will be fine

#### Instantiating Classes
- Spaceship myShip = new Spaceship();
- This instantiates a spaceship object in Java
- We can use a constructor method to also define the attributes

#### Overloading
- Allows a class to have more than one method with the same name but different parameters
- Spaceship() vs Spaceship(String name)
- Make sure objects are not instantiated in an invalid shape
- Constructors give birth to an object, but there are also Destructors

#### Destructor
- A special method that gets called when the object is destroyed
- Sometimes called a **Finalizer**
- Used if you have an object holding a resource

#### Instance Variable
- Variable for which each instantiated object of a class has a separate copy

#### Static Variable
- Variable that is shared across all objects in a class
- Also called a shared variable or a class variable
- Usually when you want to increase the variable for each instantiated object
- "Global Variable?" it's global for the objects, not for the whole program, it is shared within the class
- include the word static in the variable
	- public *static* float toughness;
- To access, use the name of the class: **Spaceship**.toughness (where Spaceship is the class name)

#### Static Methods
- public static increaseDifficulty(float t){}
- Methods are always called using the class name

**Static Methods and Variables are represented in UML by being underlined**

# Creating the Class Interface

#### Visibility
- By default, we make all attributes private and some operations, operations that need to be accessible to other objects should be made public
- + **public** the feature is directly accessible by an instance of any class
- - **private** the feature may only be used by an instance where the class is included
- `#` **protected** the feature may be used either by the class that includes it or by a subclass or descendant of that class
- ~ **package** the feature is directly accessible only by instances of a class in the same package

# Creating Associations
- An association that must support message passing in both directions is a two way association
- A two way association is indicated with arrowheads at both ends
- Minimizing the number of two way associations keeps the coupling between objects as low as possible
- Determine the direction of message passing i.e. the navigability of the association
	- Do objects of class A have to send messages to objects of class B?
	- Does an A object have to provide some other object with B object identifiers?
- If yes, then A needs B's object identifier

#### Using a User Story
*"As a Cabbie, I want to drive people to their destination in my cab so I get paid."*

- A cabbie can drive only one cab at a time. A Cab could just be a Cab Number and tyhen the attribute on Cabbie would contain just that
- If analysis of other stories found that Cab was complex and had its own attributes and was a class, Cabbie still needs a Cab
- Cabbie has a Cab (or MyCab) attribute of type of Cab
- Cabbie sends the message to Cab to move via its attribute- Cab doesn't need to know anything about the driver to move so Cab doesn't need to send a message to Cabbie, it is just waiting to be told to move