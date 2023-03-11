---
class:  web 2011
module:  module eleven
date:  2022-07-24
tags:  #objectoriented #web-2011
---

## Iterator Pattern

- Encapsulating the iteration (encapsulating what varies)
- *Iterator Pattern* provides a way to access the elements of an aggregate object sequentially without exposing its underlying representation
- Aggregate Objects
	- Arrays
	- Java Collection classes like ArrayList
	- Basically a collection of objects
		- Lists, etc
- Just want to access the elements in a sequential manner
- The iterator knows how to access the elements, the Client doesn't
- Client asks the object for its iterator
- Uses the iterator to iterate through the items in the aggregate
- Iteration code can be used for any aggregate object
![[iterator.jpg]]
- hasNext: if there are more items to iterator over
- next: returns the next item
![[iteratorexample.jpg]]
- Iterator is an interface
- Menu is an interface


## Built In Iterators
- Java's Collection classes come with iterators
- Use the iterator() method to get the iterator for any collection class, including ArrayList
- Java arrays don't have built in iterators
- **Java:** enhanced for
- **Python:** for/in
- **JavaScript:** for/of

### Single Responsibility Principle
- Every responsibility increases the chance of change
- Two responsibilities means two areas of potential change
- A class should have only one reason to change
- If we allow a class to manage the collection and iteration, there are two chances for change


## Template Pattern

- Used in Spring for remote system calls
- Provides common behaviour that spans across concrete implementations of remote calls
- Shares similar behaviour across remote calls as wel through the way the templates are structured

#### How it Works
- Common boilerplate operations are hidden in a base class
- Common flows are captured in overarching algorithms with abstract or default methods for the variant code
- Concrete implementations handle the variant code and extend the base class

#### Why Use It
- Often common code paths lead to code replication, templates encourage DRY and reuse
- Error prone code can be solved once and reused
- Common task semantics can be templatized to reduce costs of implementing new versions of same pathway

![[template.jpg]]

