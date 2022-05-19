---
class: webd 2011
module:  module three
date:  2022-05-12
tags: term-2 webd2011 
---

# Domain Modeling

### Identifying the Objects

**Conceptual Model**
- Represents important objects and the relationships between them
	- More generic "objects" not software objects
- Go through all of the use cases and user stories to pick up all of the nouns (objects)

*Gather the nouns in the Use Case Scenario*
"Dodge" Use Case Scenario: **System** spawns enemy spaceship in play area. **Spaceship** flies towards player **asteroid** and fires **missile** at **it**. **Player** steers asteroid in **direction** to avoid missile **path**. Missile flies past player asteroid and disappears **offscreen**.

*Find any obvious duplicates*
- When in doubt, keep it
- Eliminate ambiguous nouns
- Final list:
	- Spaceship
	- Area
	- Asteroid
	- Player
	- Path
	- Missile
	- Direction
- This is the beginning of a *conceptual model*

### Identifying Class Relationships
- Draw lines between the boxes based on relationships and describe the relationship using verbs
- We can add UML notation for multiplicity (it's not necessary but it can be useful)
- This is just a conceptual model to use for communication and prompt ideas
- Detailing relationships makes it easier to realize which objects interact with each other and which objects have behaviours affecting other objects
![[relationships.jpg]]

### Identifying Class Responsibilities
- We can look for verbs to identify responsibilities

"Dodge" Use Case Scenario: **System** *spawns enemy spaceship* in play area. **Spaceship** *flies towards player* **asteroid** and *fires **missile*** at **it**. **Player** *steers asteroid* in **direction** to *avoid missile* **path**. Missile *flies past player* asteroid and *disappears* **offscreen**.

- An object should be responsible for itself
	- Ex: Steering the asteroid is obvious that it will be initiated by the player BUT we should not write code in the player class, the player class should ask that of the asteroid class. The asteroid is in charge of changing its state.

![[responsibilities.jpg]]

- Some verb phrases were simplified:
	- avoid missile path -> detect collision
	- flies past player -> move
	- flies toward player -> move
	- spawn enemy spaceship -> spawn
	- fires missile -> spawn
	- disappear offscreen -> detech out-of-bounds
- Player didn't get any responsibilities?
	- This doesn't show who *initiates* the actions, just where the responsibility lies in performing them
	- The player requests things to happen from the objects!
	- An object that knows too much or does too much is called a *GOD OBJECT* it has too much responsibility
	- *Avoid global master objects*
		- If it controls everything else around it, that's more procedural
		- Responsibilities should be spread out
		- Objects should be responsible for itself as much as possible
		- Maintaining application is easier this way

### CRC Cards
- Class, Responsibility, Collaboration
- Drawn on index cards, meant to be simple
- Each card represents one clas and has 3 sections:
	- **Class Name**
	- **Responsibilities** of the class
	- **Collaborators** the other classes it interacts with
- Could also be *CRH* cards for Component, Responsibilities, Helper
- Use the nouns to help identify potential classes and verbs to help identify responsibilities
- It's okay not to have it perfect right this second bc this is just for conceptualizing

![[crc.jpg]]
- When you start to create a pile of cards, most people naturally put related objects together
- This is why you should not use an electronic model for this
- Using physical cards also causes a constraint, if you need more than one card that's a clue that you may need to redesign that class bc it has too much responsibilities
- Finish this phase with at least the names and core responsibilities for the first items you itend to code

# Domain-Driven Design

### What is DDD?
- Developed by Eric Evans
- Developed before Agile and microservices existed
- Overall design is ideal and is still applicable today

**Collaborative**
- Business people and developers must work together daily throughout the project
- Underlying philosophies are almost identical

**Modeling**
- DDD is built on the notion of modeling
- Structure of the code models one to one to the structure of the domain
- All collaborators can make sense of the structure
- Changes are made to the domain, which maps to where code changes should occur

**Incremental**
- Don't come up with big architecture before coding
- Come up with only enough architecture to solve the immediate problem
- The code evolves as you learn more about the problem and more architecture is added
- DDD follows an agile workflow

*A domain-driven design architecture is designed to grow incrementally over time*

- Changes made in the domain influences the system and the system influences the domain
- Everytime you release into the domain, users will use the code and that will change the domain to some extent, it is a cyclical process

### How Does DDD Fit With Agile?
- You cannot do DDD style design if you do not have business people in the room, it is always collaborative
- *Inspect and Adapt Loop*
	- Make a small change
	- Assess (feedback)
	- Inspect and adapt
	- Improve
- To keep the system coherent: Stories in Agile

### Stories in Agile
- A short narrative
- A couple of sentences
- Describes end user performing a domain-driven, result-oriented task
- Describes your users' work
- End result should be a good result for the user

# Bounded Contexts and Entities

### Bounded Contexts
- A natural division within a business
- Bookstore Example:
	- Warehouse and Store are both contexts; Warehouse is responsible for Shipping and Store is responsible for Sales
- What are the responsibilities of the people working within that context?
- Within each context, you have distinct people working who aren't really thinking about other contexts
- Allocate communication between contexts to one small object

### Entity
- Much like an object or class in the object oriented world
- Has one job, does one thing
- Does that in specific context

**Aggregate** is a collection of entities you talk to through a single portal
- Line between entity and aggregate can be fuzzy
- Portal into aggregatre looks like an entity
- Portal entities use other entities in aggregate to get work done
- Whether something is an entity or aggregate may not be visible from the outside of the context

**Portal Entity** uses other entities within an aggregate to accomplish tasks
- Contexts are usually implemented as aggregates but might not be

### The Ubiquitous Language
- Within a given context, the people who are working in that context use a language of their own
- The language of one context is different from another
	- Bookstore Example:
		- Sales Language: Author, Readability, Length
		- Warehouse Language: Width, Size, Weight
- *The language itself will be reflected within the code*
- You will use this when talking about problems
- Used at domain level to describe work
- Ubiquitous within a specific context
- Look at the way you describe something and see which language is most appropriate
- Distinguish between actors and roles (tasks)
- Entities named after roles, not actor

**Every entity in domain-driven design should be associated with only one context**
- Every entity should be associated with one context
- Move away from relational database thinking
- Bad to have single product-object in multiple contexts because it will be too big and hard to maintain
- Contexts will have completely different databases

# Behaviour Driven Development

### Agile in Context
- BDD emphasizes the client's perspective
- Agile is used to build acceptance criteria via user stories
- User Stories are not the same as requirements

### TDD (Test-Driven Development) Historically
- The Dark Ages
	- Promoted the idea that a developer should never test their own code
	- Created tension between developers and QA departments
- Kent Beck Rediscovers TDD
	- Creation of XP from which test-driven devewlopment evolved
	- Developers should spend 20-25% of their time developing tests
- The TDD Process
	- Write a failing test
	- Write the code that allows for passing test
	- Refactor
	- Repeat
- Where does TDD Fall Short?
	- Developers want to know what to test, how much to test, and how to understand failing tests
	- Without clear guidelines as to what should be tested, confusion and misunderstandings are common

### BDD (Behaviour-Driven Development)
- In 2006 blog post: Dan North presented argument for different approach to TDD
- Allows developers to know what and how to test
- Taken from TDD and Agile to combine the needs of BAs and developers into a single framework
- Business needs are defined in code and are testable
- Consider behaviour of what you want to build first instead of tests
- Encourage writing tests with expressive names in the form of a sentence
	- Makes it clear to stakeholders what it's supposed to do

### Why BDD?
- Comes from the failures of the traditional model of software development
- Changes our understanding of how project management works

### Building the Right Thing
- It is difficult to build the app that stakeholders actually want
- Without a clear understanding of what should be built, the product will not reach its potential
- BDD is not for discovering what product to build, product owners should have a clear conception of what the product is
- BDD is for building the correct product that end users want

### Starting Point for BDD
- Product owners already understand what product they want
- Acceptance Criteria should be defined
- User Stories should be defined

### Example Mapping
- Before utilizing a user story in development, you must clarify and confirm acceptance criteria
- Example mapping facilitates the conversation to explore the problem domain
- Example mapping provides a visual representation of a user story

**Example Mapping Cards**
- Built as we have our conversation
- Begin with yellow card with the name of our story
- Blue cards represent specific rules that could strain the scope
- Green cards have examples of user story, placed under relevant blue card
- Red cards contain questions that cannot be immediately answered

### Describe Your Feature
- BDD is about providing concrete examples
- Seeks to qualify the acceptance criteria by having discussions about those concrete examples
- Concrete Examples:
	- User stories detailed and full of context
	- Well defined examples allow for robust and focused tests
	- If examples are too abstract, it will be difficult for developers to write tests
	- "Can you give me a specific example?"
		- As a barista, when I came into work early monday morning, I saw we were running low on Colombian Dark Roast, I logged into the system and ordered two bags of Colombian Dark Roast.
	- We Need:
		- Names
		- Context
		- Situational Awareness

*Acceptance Criteria vs. Scenario*
- Acceptance Criteria
	- Addresses what defines a working system
	- Written as pass/fail
- Scenario
	- Defines the initial conditions for acceptance criteria
	- States the trigger of scenario and expected outcome

### Primary Perspectives
- Client
- Developer
- Tester

Scenario Format
- Scenario: a user story
- Given: some set of initial conditions
- When: an event occurs
- Then: an outcome is expected

# Give Me An Example

### Three Amigos Meetings Benefits
- Shared understanding of work increments
- identification of issues early in the process
- Defining clear acceptance criteria
- Allows for each of the primary perspectives to have buy-in for project
- Three Amigos represents three different perspectives

### Gherkin Specifications
- We need a way to translate acceptance criteria into executable tests and confidently build the correct application
- *Gherkin* is a business-readable, domain-specific language that describes your software's behaviour, but not how that behaviour is being implemented
	- Automate testing
	- Acts as documentation
	- Provides structure for documenting examples of desired behaviour
	- Saved as plain text, line oriented, using indentation to define structure
	- Language is semantic
		- Feature (every file begins with this keyword) followed by the actual feature
		- Scenario - a single concrete example of how a system should behave, written as pass/fail examples, each feature has 5-20 scenario
		- Given - describes the context or precondition for the scenario
		- When - the action being taken on the system by some actor
		- Then - provides the expected outcome to the scenario

# Noun Analysis
- Noun analysis consists of analyzing the software request (user story or use case) to find links in info andd business concepts
- All nouns represent info that must be represented and accounted for in code

### Word Types
- Noun
	- Actor, Class, or Attribute
- Adjective
	- Attribute, Specialization, or dropped if not relevant to Methods
- Verb
	- Method on the class affected by the action
- Adverb
	- Possibly included with a Verb if multiple variations exist in the same class as part of the name
	- Possibly a parameter if an alternate outcome is apparent in other stories

### What Makes it a Class?
- An Actor uses the system, they are not a class unless you have to specifically store or retrieve info about them
- An Attribute is a Noun that directly describes or provides context for another Noun
- A Noun becomes a class if it has 1 or more Attributes or Actions found

### What Are the Attributes?
- A noun is an attribute of another noun if it "belongs" to it or helps describe that noun
- If a noun has attributes, this means that it is a class because you have to store data about it
- If the noun is the actor and there are no other attribute requirements explicitly defined in the stories then it is not a class
- If your noun is the entire system, it is also ignored

*Sometimes, a noun is a complex concept but it is still just an attribute, don't make it a class if it doesn't have to be.*

**As an instructor, I want to know the letter grade associated with a given student's mark.**
- Nouns: Instructor, grade, student, mark
- Verbs: know, given (this data will be provided, not an action that requires implementation; given indicates a parametre on a method or another attribute, not a real action)
	- Verbs are obscure here so we may need to reword before continuing to make it a little more understandable
**As an instructor, I want to get a student letter grade associated with a given student's mark.**
- Same type of sentence but adjust the action words to be more clear
	- Get the StudentLetterGrade
- Relationship between a Mark and a Letter Grade is missing
**As an instructor, I want to get the student letter grade with a given student's mark that is above its low value and below its high value.**
- Additional nouns: low, high value
![[grid.jpg]]

# Testing
- The problem with Waterfall is that the requirements were wrong and no one noticed until the end
- The problem with V-Model is the testing still generally confirms what the development team already knows and the testing is systemic until the end
- Think about testing before you start developing
- We develop the test plan before coding starts to know what the user knows

**Happy Path:** This is the way the system will be used, most likely. It is  generally what the user is thinking about when the story was requested. It is the most basic test.
**Extremity:** This path tests extreme values, what the worst case is that the test will go through and still gives the expected result. What are the highest/lowest values we need to test? What are the other possible states of objects we will run into?
**Exception:** This is what happens when values are not provided as expected. What would happen if a value had something different than expected?

**Given** – a current state, business concepts and values that indicate a starting place
**When** – a single action to be performed. A single action may be many behind the scenes of course. This is a behavior/event from a business users perspective (e.g.  ‘A sale is completed’)
**Then** – This should indicate everything the user expects to see when this occurs (e.g. ‘The customers payment is taken and a receipt detailing all products purchased is printed…. Etc.)

