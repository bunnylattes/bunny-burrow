---
class:  web 2011
module:  module nine
date:  2022-07-20
tags:  #objectoriented #web-2011
---

# Decoupling

### The Observer Pattern
*Loose Coupling* means to strive for loosely coupled designs between objects that interact. Objects are loosely coupled when they interact with each other but don't know much about each other. They don't become too dependent on each other and it keeps the design more flexible. Minimizes the complexity of the scenario when a lot of objects are coming and going.

![[observe.jpg]]

- Subscriber objects can request to become a subscriber of the Publisher object. Once they do, they will receive data from the Publisher, ever changing data as well
- There can be non-subscriber objects as well

*The Observer Pattern* defines a one-to-many dependency between objects so that when one object changes state, all of its dependents are notified and updated automatically.

- The Subject is the Publisher and the Dependents/Observer are the Subscribers
- The Subject being the owner of the data makes for cleaner system organization

![[observers.jpg]]

- Subject is an interface and the Concrete Subject MUST implement the same methods as the subject
- There is an Observer interface as well that is a superclass for the Concrete Observer objects
- The Concrete Subject has a Concrete Observer

*public interface Subject {
	public void registerObserver(Observer o); // allow observers to register themselves
	public void removeObserver(Observer o); // allow observers to stop participating
	public void notifyObservers(); // notify the observers if data changes
}*

#### Loose Coupling
- Subjects and Observers are loosely coupled because they interact but have little knowledge of each other
- Subject knows only that the observer implements a specific interface
- Subject doesn't need to know the concrete class of the observers
- Any class can implement the Observer interface
- Subject relies on a list of observers
- Observers can be added, removed, or replaced at any time
- Subject does not care, it just maintains a list of observers and notifies them
- Subject does not need to be notified of a new observer
- Subject and Observer changes never affect each other


# Application Structure Patterns

### Layered Architecture
- Each layer has a distinct responsibility
- The call of the code flows downwards
![[layered.jpg]]
- You can add more layers if necessary or merge layers
- *Advantages*
	- Well known among developers
	- Easy to organize
- *Disadvantages*
	- Lead to monolithic apps
	- Need to write a lot of code


### Microkernel / Plug In Pattern
![[microkernel.jpg]]
- Task schedulers
- Workflows
- Data processing applications
- Browser extensions
- *Advantages*
	- Flexibility
	- Clean separation
	- Separate teams possible
	- Add and remove functionality at runtime
- *Disadvantages*
	- Core API might not fit future plugins
	- Can the plugins be trusted?
	- Not always clear what belongs in the core


### CQRS: Command Query Responsibility Segregation
- Two models: read/query and write/command
- Allows for scenario specific queries
	- Improved performance and reduces complex queries
- Synchronization required
- Different from event sourcing
![[cqrs.jpg]]

- *Advantages*
	- Simpler read queries
	- Less joins
	- Faster and more scalable read queries
	- Maps better to the business language and makes it easier to communicate with stakeholders
- *Disadvantages*
	- Added complexity
	- Learning curve
	- Possibility of data inconsistencies
	- Eventual consistency but not immediately


### Event Sourcing
- Store events instead of current state
- Event = something that happened in the past
- Rehydration or replay: Apply all previous events to a new object to find what happened in the past
- *Advantages*
	- Trace of events
	- Audit trail; insight into when events occured and what triggered them
	- Business language; easier for stakeholders
	- Event replay can show bugs
- *Disadvantages*
	- Replay and external systems could lead to issues in systems
	- Event structure changes can be triggered
	- Large number of events can make it slow
		- Snapshots are a good solve for this
![[eventsourcing.jpg]]


### CQRS and Event Sourcing Combined
- Two different concepts but can be powerful when used together
- *Advantages*
	- Simpler and faster queries
	- Scalable
	- Trace of events
	- Audit trail
	- Business language !
- *Disadvantages*
	- Added complexity
	- Learning curve
	- Data inconsistencies
	- Event structure changes
![[cqrsecebt.jpg]]