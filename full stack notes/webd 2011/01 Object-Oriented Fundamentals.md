---
class:  web 2011
module:  module one
date:  2022-03-02
tags:  #objectoriented #web-2011
---

# Object Oriented Fundamentals

### Object Oriented Thinking

- Each object contains its own data and logic to describe how it behaves and interacts with other objects
- Object Oriented Approach: code re-usability
- Programming paradigms: a set of ideas that is supported by many languages
- Every object has inherent properties (characteristics) that describe its current state, they are independent of other objects because they are separate objects
- Every object is self contained, its own attributes, and own behaviours
- Objects = nouns: if you can put "the" in front of the object, it is an object

**Classes**
- A class is the detailed description of what an object will be
- Once we've written and defined the class, we can create objects
- The class comes first: you can't make round cookies without a circular cutter

**Method**
- A program procedure that can return a value
- Defined as part of a class
- Can only access data known to the object

**Instantiation**
- Each object created is an instance of a class

**APIE: A Pie**
- Abstraction
	- "person" you understand the idea of a person to abstract the idea of what "person" is
	- we focus on the essential qualities rather than one specific example
	- discard what is irrelevant re: person: name, height, gender is important but favourites isn't
	- classes focus on the essential qualities we care about
- Polymorphism
	- ***Dynamic/Runtime Polymorphism***: uses the same interface for methods on different types of objects
	- ***Overriding***: re-writing a method that was inherited from a superclass
	- ***Static (Compile-Time) Polymorphism***: Method Overloading allows you implement multiple methods within the class with the same name but with different types of parametres that create a different output with similar functionality
- Inheritance
	- Base a new class on an existing one
- Encapsulation
	- Black Boxing: closing off the process 
	- Reducing dependencies between different parts of the application, no domino effects when changing code
	- Encapsulate as much as possible

### Object Oriented Analysis, Design, and Programming

- **Analysis**: What do you need to do? What's the problem?
- **Design**: How are you going to solve the problem?

#### Five Step Approach
1. Gather requirements
2. Describe the application
3. Identify the main objects
4. Describe the interactions between objects
5. Create a class diagram

#### Unified Modeling Languages (UML)
***Standardized notation for diagrams to visualize object-oriented systems***

**Required on UML**
- Name
- Attributes/Fields
- Behaviours/Methods

**UML Tools**
- Commercial or open source
- Support platforms
- Drawing applications

<a href="https://en.wikipedia.org/wiki/List_of_Unified_Modeling_Language_tools">LIST OF UNIFIED MODELING LANGUAGE TOOLS WIKIPEDIA</a>
- You can find all of the info about UML tools here

## Programming Paradigms

### Procedural

- The analysis is action oriented so it’s very easy to program this way. People think in terms of steps they (or a process) needs to perform in order to get a result, that is how everyone is initially taught to break down problems. When I want a cup of tea I think of boiling the water, adding the water to the cup, steeping the tea, then I get to drink it. Simple. How I combine the boiling water and tea with the devices available would be in the process itself, passed as parameters to actions that need them.
- Because it’s so easy to do and understand, this was the first way programming was done. It’s still quite common especially with the popularity of script programs like Powershell but in order to not cause more problems than it solves it should be used a certain way.
	- The process is a small and simple one without integration or interaction
	- The process is internal to the IT department, no outside user involvement
- Why is that? The longer the process, the more actions you need to get to your result. A big long process with action after action is hard to debug and find an issue so you often have to simply start at the beginning and walk it through line by line until you find the problem. Some say that it’s because procedural code is not re-usable but that’s not the case. You can create re-usable action based code, it’s just much harder to work with later in a larger code base.

### Object-Oriented

- Along comes Object-Oriented to solve all your problems and combine your code in ways that makes them easy to maintain. Well yes and no. There are 2 big requirements for proper object-oriented programming if it’s going to help you keep your large code base easy to maintain.
	- Behaviors and the data they need are stored in the same class. Parameters should only be needed if the action needs data that is not normally attributed to the class (not needed for anything else) as well to complete. The action depends on the data in the object at the time the action is executed, known as the objects State.
	- The classes, attributes, and actions are created and stored in the language of the business.
- In the language of the business is generally missed, and is the reason many don’t see the value of created a solution with a complex object oriented paradigm. If you create your program in the language of your business though, whenever your business needs something changed in the program they will actually talk to you in the language of your program.

#### Incomplete Truths

1. Object Oriented development was created to make code more reusable
	- Procedural code is action oriented, that doesn't mean you can't break a problem down into many actions and re-use them. Consider a baking recipe, I have a recipe for making buns that contains the actions I need to perform to finish them as cinnamon buns. However I also have the option of turning them into cheese buns by following the cheese process instead. I don't have 2 entire recipe's, I just follow different actions at the end, The actions have different parameters, cheese instead of cinnamon.
	- Of course If I were writing this recipe to share I would need to plan more carefully how the actions could be re-used. Can the cheese action be re-used on say Mini Pizzas for the kids? Not without careful planning and documentation.
2. Procedural is sequential, so they made object oriented development.
	- All code is run sequentially, so the term sequential here likely means steps all lumped together (which we disproved above), however I'll discuss sequential as the term means as well. The process is simply what starts the code and where in the code does that call take it. A computer cannot decide to run code out of order, it does simply what the program tells it, step by step, in sequence.
	- As systems get more complex, it becomes harder and harder to see the sequences. The content of the sequences become spread out. Asynchronous processes allow multiple sequences to run at the same time. When you really evaluate the processes though, they will all be sequential. Object oriented development simply helps you better keep track of how sequences relate. 
	- All programming is sequential, Only the actor can change the sequences but they are still sequences


### Functional

- Some equate functional as a throwback to procedural but it’s not quite the same. In procedural code, everything is actions. You supply the data an action needs as a parameter when it's executed so the action can perform it's duty. In functional code, everything is an action, however all actions are also data. When you call an action, you supply the actions it needs as parameters to execute and perform other actions. This can get very complicated, but can be very powerful, especially where mathematical or algorithmic software is involved.
- A lot of developers really like to use it though because it is an action oriented paradigm which makes understanding and solving complex problems easier for them. Since functional programming is stateless, they only have to know and understand exactly what's been provided to the action at the time it is called.