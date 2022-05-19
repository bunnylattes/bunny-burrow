---
class: webd 2010
module: module 12
date: 2022-04-28
tags: webd-2010 project-management Agile 
---

# Agile Tools and Techniques

### Behaviour Driven Development
- Enhances the communication between business users and the development team by communicating using examples which are more concrete for the customer
	- Many people are uncomfortable with abstractions and prefer to work with real examples
- As models change, examples can be refined by building on previous examples
	- System behaviour may change per user role, scenario variation (user action), data, business rule
- IIBA extension views Specification by Example to supplement existing analysis techniques however some believe it should or can be the primary analysis technique

### Guidelines for Examples
- Examples and models should be at a level of granularity that is appropriate for the outcome you seek
- Use examples to derive acdeptance criteria, help the developer design the solution, and as a foundation for functional testing
- Examples may also be known as scenarios
- Should not be artificial or made up
- Business analysis activities help to facilitate the discovery of the examples and ensure that the set of examples is comprehensive
- Not all examples identified will necessarily be within the scope of a development effort
- Typically, examples are written to provide a simple grammar format that allows real scenarios to be filled in
- Number of software products that will take examples in this format will allow them to be easily converted into automated tests, thus enabling more agile delivery

**GIVEN: (a context)
AND: (a pre-condition)
WHEN: (an action is performed)
THEN: (a testable outcome)**

*Example: ATM Positive Case*
**GIVEN**: I'm performing a withdrawal
**AND**: from "Credit Card"
**WHEN**: I request $20
**THEN**: I receive $20
	**AND**: My account balance is reduced by $20
	**AND**: My card is returned

*Example: ATM Negative Case*
**GIVEN**: I'm performing a withdrawal
**AND**: from "Credit Card" and the account is NSF
**WHEN**: I request $20
**THEN**: I receive no money
	**AND**: My card is returned

### Why Only Requirements by Example?
- Premise: Most effective way of checking requirements is to use test cases very much like those testing a completed system
	- Think about how the finished system will be used and then double check the reqs armed with this knowledge
- Black-box test scrips are by nature very precise and contain clearly defined steps and values, unlike traditional reqs which are generally a lot more abstract
- Every time examples show up in a software project, people have to re-invent them
	- Customers and business analysts use one set of examples to discuss the system reqs
	- Developers come up with their own examples to talk to business analyst
	- Testers come up with their own examples to write test scrips
- As illustrated by the telephone game, these examples might not describe the same things
- With enough examples, we can build a full description of the future system which are discussed to make sure that everyone understand them correctly and get a good set of tests
- Examples can become Tests that verify Requirements 
- Examples can elaborate on Requirements
- Realistic examples contian precise info and they ask for precise answers
	- Makes people think harder and not brush the question off
- Identify edge cases, negative paths, and scenarios in which things do not go according to plan and discuss them as well
- Ensure you cover off
	- Normal use
	- Abnormal but reasonable use
	- Abnormal and unreasonable use

### Steps to Implement
1. Use real world examples to build a shared understanding
2. Select a set of these examples to be a specification and an acceptance test suite
3. Automate verification of the acceptance tests
4. Focus the software development effort on the acceptance tests
5. Use the set of acceptance tests to facilitate discussion about future change requests, effectively going back to step 1 for a new cycle of development
6. Automate the verifications

**Tables can be helpful to indicate data for scenarios and permutations**
- Determine the structure of the table, making sure that the headers cover all possible cases
- Complete the individual entries in the table

### Live Specification
- Executable code is often the only thing that we can really trust in software systems
	- Other artifacts such as specs, reqs, quickly get out of date and cannot be trusted completely
- However, executable code is unusable as the basis for a discussion with business people
- As an alternative, an automated acceptance test suite, connected to the executable code, can easily be run to check whether it still reflects reality
	- We can have the same level of confidence in the automated acceptance tests as we do in the code
	- Takes serious commitment to execute

### Examples into Tests
***Guidelines for Tests***
- Keep the tests human readable and automate them
	- If developers write tests, then they often turn out to be too technical and action-oriented
	- If the business analysts or testers write them, they often have to be changed so that they can be automated
	- A better solution is to write the tests collaboratively
- If a single person is charged with writing the tests, the person must:
	- Understand they must research realistic examples and interview domain experts on expected behaviour
	- Cannot make up theoretical examples and definitely not provide the answers themselves
	- Probably suited best to a business analyst

# Real Options
- To help people know when to make decisions rather than how: Delay making a decision or a commitment in a project until the last responsible moment, when the decision really needs to be made
- *Three Rules*
	- Options have value
	- Options never expire
	- Never commit early unless you know why
- Avoid commitments and keep your options open and understand when an option expires so that you can actively manage whether you chose that option or let it lapse
- Real options address people's aversion to uncertainty by providing the conditions when a commitment should be made rather than waiting
- As options have value, pushing the expiry date back adds value to your project and allows you more flexibility
- Common usage:
	- Customers chose which item to invest in next
	- Next sprint planning session
	- In Kanban, the next time capacity becomes available to work on something new
- Options are things you can chose to do or not do
- If you are committed to doing something and there is only one way, then you do not have options
- Examples of not-options:
	- Things you cannot do
	- Things you cannot afford
	- Things you cannot do in time
	- Things you cannot buy or sell
	- Things you do not have tools for
- When looking at options, we want to assign criteria as to when to make a decision
	- Reduces emotional commitment
	- Specify the conditions when the decision should be made

![[dec.jpg]]
### Advantages
- Simplify decision making by providing a simple set of principles to follow
- Decision making occurs quickly as you only focus on the immediate decisions and defer prioritization until complexity is resolved
- Does not tell you how to make decisions, just when
- Forces us to consider the decision points and the information arrival process (when data arrives and whether it arrives before the decision)

### Disadvantages
- Can be counterintuitive as they require us to analyze systems from the outputs to the inputs
- Not a simple process to be followed, requires patience and study

# Kano Analysis
- Helps an agile team understand which product characteristics or qualities will prove to be a significant differentiator in the marketplace and help to drive customer satisfaction
	- Either because they are exceptionally important or because their absence will cause intense dissatisfaction
- Two axes:
	- Extent to which the feature is implemented in the product
	- The level of customer satisfaction
![[Pasted image 20220428223357.png]]

- The graph represents product characteristics that should fall into one of three categories:
	- **Threshold Characteristics (Fundamental)**
		- Those absolutely necessary for stakeholders to consider adopting a product
		- Absence will cause intense dissatisfaction but, as they represent minimum acceptance criteria, their presence will not increase customer satisfaction beyond a certain low level
	- **Performance Characteristics (Linear)**
		- Those aspects that the delivery of the characteristic produce a fairly linear increase in satisfaction
		- Represent what customers expect to see in a product
	- **Excitement Characteristics (Delighters)**'
		- Significantly exceed customer expectations or represent things that the customer did not recognize were possible
		- Presence will dramatically increase customer satisfaction
- We need to determine the category to which a characteristic or feature belongs by asking two questions for each feature:
	- *Functional Form:* How do you feel if this feature or characteristic is present in the product?
	- *Dysfunctional Form:* How do you feel if this feature or characteristic is absent in the product?
![[kano.jpg]]

# Value Stream Mapping
- Learn manufacturing technique
	- Illustrates the flow of information (or materials) required for a process
	- Used to identify areas of potential improvement in an end to end process
	- Graphical representation that captures a snapshot of the value stream
- **High Level Process**
	- Identify the product or service
	- Create a value stream map of the current process, identifying steps, queues, delays, and information flows
	- Review the map to find delays, waste, and constraints
	- Create a new value stream map of target state
	- Develop a roadmap for creating the optimized state
	- Revisit the process in the future to continually tune and optimize it
- Used to help re-engineer business processes or re-engineer and tune the software development process itself, for example, to reduce lead time from product discovery to release

### Value Stream Mapping Steps
- Observe or simulate value stream
- Follow a product path by starting at the end and recording the process working your way backwards to the beginning
- Draw the *Current State Value Stream Map*
	- Capture the information flow including things such as orders, schedules, inventory time, changeover time, cycle time, and number of operators involved
	- Show each step in the flow with hands off and sequence
		- Identify opportunities for improvement in the process, include time/cost values onto the steps in the process
		- Validate the value stream map before proceeding to the improvement phase
- *Analyze Current State*
	- Identify value adding steps from those that are non value adding
		- Non value adding steps can be analyze further to determine which ones are necessary (such as meeting regulatory requirements) and which ones are unnecessary (such as excessive paperwork)
- Draw the *Target State Value Stream Map*
	- Identify improvement areas
		- Unnecessary non value added steps are the source of waste and, as such, they can be aliminated
		- Draw the value stream map to show the value stream after aliminated waste
		- Identify supporting material required for implementing the improvement such as training and changeover
![[streammapping.jpg]]

### Advantages
- More comprehensive than a process flow diagram
- Provides a blueprint for implementing improvement
- Establishes a shared understanding of process wastes and bottlenecks

### Disadvantages
- Not easy to construct in comparison with other visual modeling techniques
- Can look daunting because of all the info captured
- Easy to get caught making the value stream map complete and perfect instead of proceeding to the improvement stage
- Doesn't work well in non-linear work
- Leads to disruptive or "re-engineering" approach, doesn't work well with ongoing improvement efforts