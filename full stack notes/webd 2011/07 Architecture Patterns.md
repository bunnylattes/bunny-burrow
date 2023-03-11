---
class: webd 2011
module:  module five
date:  2022-05-12
tags: term-2 webd2011 
---

# Adding Architechture Patterns

### Application Landscape Patterns
***Solution to a common problem that defines components and the interactions between them.***

#### Examples
- Repository
- Singleton
- Builder
- Factory

#### Repository
![[repository.jpg]]

- Shows us how we can show and interact with multiple classes and how to organizae multiple applications

#### Using Known Patterns
- Akin to using a blueprint to build something that will be better structured
- Makes code recognizable to other developers
- Helps decision making process and senior devs spend less time coaching
- Easy to maintain
- It's already proven to work

#### Caveats
- Other solutions are possible
- No guarantee that it will work; it can be a good starting point if it doesn't work perfectly

#### Difference Between Software Patterns and Design Patterns
- Design Patterns:
	- Small amount of components
	- Part of a larger application
- Architecture Patterns:
	- Defines a significant part of the application
	- Many components
	- Mostly paradigm independent

#### Categories
- Application Landscape
	- Figure out how the neighbourhood is structured
- Application Structure
	- Designing/Building a house
	- Single executable
	- Can be part of a larger application landscape
- User Interface
	- Figuring out how people get into the house
	- How the user interacts with the application itself
	- Model-view-controller (MVC)

#### Monolith
- Application that is a single executable that is deployed but may need some other components that it needs but they are deployed and executed together
- It contains all the logic needed to solve a problem
- Advantages:
	- Simple, easy to understand, implement, and test; easy deployment; ideal for limited scope
- Disadvantages:
	- Tight coupling; easily leads to complex code; one size fits all for every subdomain
- Monolith is not synonymous with badly structured code

#### N-Tier
- Multiple tiers, tier performs specific task, tiers can be physically separated, tiers are not layers, technical boundaries (not functional ones)

#### 3-Tier
- **Presentation** Tier: UI and pure UI logic
- **Business** Logic Tier: Business Logic
- **Data** Tier: Databse
- These can be together or separated
- Data flows from Presentation to Data without skipping Business
- Advantages:
	- Independent development, only have to modify one tier
	- Scalability
- Disadvantages
	- Changes ripple through tiers

#### Service-Oriented
- Multiple services
- Each service is a business activity
- Service composability
- Contract standardization
- Enterprise service bus

![[bus.jpg]]
- Advantages:
	- Services loosely couples
	- Scalability
	- No duplication of functionality
- Disadvantages:
	- Reduced agility and team autonomy
	- Costly
	- Many differing views

#### Microservices
- Multiple services
- Each service is a business activity
- Teams run the service
- No logic-heavy enterprise service bus
- Maximum automation (tests, deployment, monitoring)

![[micro.jpg]]
- Advantages:
	- Services are independent making them scalable
	- Increased agility
	- Reliability (bc of automation)
	- Designed to handle failures
- Disadvantages: 
	- Boundaries are not always clear
	- Communication patterns can become complex

#### Serverless
- Backend as a service
- Function as a service

#### Backend
- Own application for business logic
- Many 3rd party services for other concerns (cloud)

#### Function
- Multiple pieces of code called functions
- Can contain any state
- Managed by 3rd party vendor and integrate with others
- Advantages:
	- Scaling is easy; when it's requested, it just makes more functions
- Disadvantages:
	- Constraints of the framework
	- Not easy to switch vendors
	- Tricky to maintain state memory
	- Cold Start: when first function takes slower to start up

#### Peer to Peer
- No central server; it is a network of applications
- No constant connection
- Dynamically discoverable
- Machines don't have to be connected to all the other machines
- Sometimes a central server is added to notify about a new machine
- **Sharing Resources**
	- Processing power
	- Data
	- Memory
	- Storage
- Cost effective!
- Scaling is easy: just add more applications or machines to the network
- Disadvantages:
	- Possible security issues bc of decentralization
	- Only for specific scenarios
	- Nontrivial to code

#### Microservices
- Can be traced to SOA and other patterns
- Decomposition: breaking a software problem into smaller pieces that are easier to understand and solve
- System Decomposition: Breaking a system into smaller units that make it easier to solve a series of system problems; the right size for the use cases
- All communications over ReST
- Polyglot development support
- Each unit of work can call from any other unit of work
- Cheap; entire thing can be done with open sourced software

**Compromises are always needed to be made.**

- Cost will gradually go up