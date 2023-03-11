---
class:  web 2011
module:  module twelve
date:  2022-07-24
tags:  #objectoriented #web-2011
---

## State Pattern
- **When to Use:**
	- When we have a class that can be in several different states and needs to behave differently depending on which state it's in
	- Need a readable and reusable way to change the behaviour of this object
- The behaviour changes depending on the state of the object
	- ex: an order that could be not shipped, in transit, delivered, etc
- The State Pattern's solution:
	- Represent the behaviour for each possible state of a class as its own class and then defer the state-specific logic to an instance of the appropriate class

![[state.jpg]]
- State Interface 
- Each possible state is its own subclass and the behaviour is defined by the subclass
- The object that is affected by the state is then going to contain an instance of one of the implementations of this state and will call the method
	- currentState: do something that will call the appropriate method


## Gateway Pattern / API Gateway
- Problem: Client ability to call any service can create chaos
- Gateway provides a facade/proxy
- Single layer that proxies, mutates, or limits calls
- Can become a single point of failure

#### Mutation Behaviours
- Can simply proxy
- Can decorate payloads
- Can aggregate
- Can limit access
- Movement buffer

#### Strategy
- Define contracts
- Expose APIs for those contracts, client focused
- Adhere to strict version control and passive changes only
- Implement the gateway to call your services and your clients to call the gateway


## Process Aggregator Pattern
- Problem: You have several business processes that must be called together and have a composite payload