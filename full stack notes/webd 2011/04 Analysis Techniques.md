---
class:  webd-2011
module:  module two
date:  2022-03-15
tags:  #objectoriented #web-2011
---

# Analysis Techniques

#### Overview
- Analysis: Discovering and connecting the big picture
- Product Analysis Discovery:
	- Who the users are
	- Goals
	- Available data
	- Rules and decisions
	- Gaps
- Helps us ensure complete requirements, showing people the same tree
- Brings the details that have not been thought of and balancing detail

***Thinking, Dialoguing, Modeling, Diagramming, Organizing***
- Stakeholders see the solution differently and we need to help them understand by using models and diagrams
- Stakeholders think about the product in terms of what they can SEE
- Elaborate techniques, informal convo, analysis techniques vary by level of formality
- **Variety is required!**
	- Strategic combo of techniques that work best to engage stakeholders and customers

### Process Models
- Creating a visual to explain a process or sequence of activities
- Most commonly used technique
- Ignite dialogue on the team
- See where details fit into the big picture
- Visualize the process
- Organize requirements
- Analyse details of the product/system
- Process models need to be simple so that stakeholders can read the model without a tutorial
- Formal process models are for more detailed analysis

**Process Model Principles**
1. Know what you are modeling: current state or future state? Typically, you are defining the future state with requirements. Do not focus too much on the current state.
2. Progressively elaborate and build in layers: try not to put all the detail into a single model.
3. Make it action oriented and be specific: name the process and its activities.
4. Avoid using ambiguous words like manage, process, handle, etc. They build false concensus and force developers to interpret or guess what is needed.

### Context Diagrams
- Shared Understanding: techniques that get everyone on the same page.
- Start with the big picture, context!
- **Context Diagrams** provide a view of the system or product in its environment, including the people and systems it interacts with.
- Helps teams identify scenarios, users, user goals, etc. Helps the team stay out of the details until we understand the big picture.

#### Case Study (Coffee Place)
- Domain: Order Online
- Key Roles: Customer (Primary), Manager, Order Specialist, Shipping Specialist
- Key Internal and External Systems: Payment Processors (PayPal & Credit Card Processor), Data Store
- Explore Interactions between Roles or Systems with the Domain

**Tips**
- Do not connect the user roles to each other or the rectangle entities
- Keep it to 15 total arrows
- Do not make a technical architecture diagram of the technical components

### User Stories and Story Mapping
- **User Stories:** Placeholders for future conversations
	- Who/Role, What/Goal, Why/Benefit
	- As an online shopper, I want to provide a credit card on file so that I do not need to re-enter my credit card information each time I make a purchase
	- **Acceptance Criteria** shows the details of what success looks like from a user point of view
	- **Story Splitting:** When splitting a story, we keep it from a user POV and avoid splitting by technichal component or team activity. Splitting stories breaks down the stories into smaller pieces for better analysis.
- **Story Mapping:** Map how the users relate to one another
	- Organizing user stories through visual format helps to see the big picture
	- Keeps the team focused on the user experience
	- Take the stories and put them in sequenceof user experience

### Decision Tables
- Organize and display decision logic
- if/then conditions
- Define the results in the last column
- Have conditions be binary
- 2-4 conditions to make table smaller

### Data Flow Diagrams
- Provides a visual of the processes and data that flows through them

### State and Sequence Diagrams
- Show difference states something can take
- Shows all the states and what causes the states to change

## Waterfall
- All of the requirements are gathered and analysed first in great detail
- The development process then runs until the entire application is complete, at which point it's delivered or deployed
- The process runs from start to finish with no deviation or looping back

![[Pasted image 20220315175524.png]]

#### Development Techniques
**Prototyping**
- To try and help reduce risk of change, a prototype of the project can be shown to the project sponsor for early feedback and proof of concept
- There was only one point of feedback near the beginning (not good)
- The prototype was usually hacked together and would become the app (bad)

**Personas**
- Requires development of extremely detailed fake user profiles
- Helps developers with no real user feedback options attempt to think like the users they are developing software for
- Long term can prove out to create a better user experience and more user-focused developers

#### Advantages
**Easy to Budget:** The project is designed in its entirety up front and so it's easy to estimate reasonably accurate costs
**Easy to Manage:** There are no deviations or decisions other than move onto the next phase when this phase is delivered

#### Disadvantages
**Rigidity:** While its advantages are based in this, it's also a disadvantage:
	1. There can be no change in requirements
	2. The problem being solved cannot change as this process will deliver what was asked for
	3. No allowance for missed requirements
**No Feedback:** The solution is provided in the end so no chance for user input once they've seen it

#### When to Use
- The project is of small duration (it can finish before changes may be required)
- There is no developer collaboration needed or if collaboration is difficult due to remote teams
- There is a low risk of requirements changing
- There is a need to have mroe precise budgeting


## V-Model
- Nearly the same as waterfall with heavier focus on testing
- Testing is planned in parallel to the corresponding design task
- Decreases the likelihood of an invalid application making it to production
![[Pasted image 20220315184000.png]]

#### Advantages
**Easy to Budget:** The project is designed in its entirety up front, easy to estimate cost
**Easy to Manage:** No deviations or decisions other than move onto the next phase
**Requirements are validated before coding:** Test planning and development is parallel to the design and development process

#### Disadvantages
**Rigidity:** 
	1. There can be no change in requirements
	2. No allowance for missed requirements
	3. If you try to account for changes, you must revisit testing and design
**No Feedback**

#### When to Use
- Project is of small duration
- There is no developer collab or it is difficult
- Low risk of requirements changing
- Need to have precise budgeting
- Quality assurance concerns

## Interative/Incremental
- Assumes requirements could change by the time we get to coding so it brings gathering requirements closer to the actual coding of those requirements
- Each iteration runs through its own waterfall (sometimes called Rapids)
- Usually termed **Watergile** as an incorrect Agile implementation usually looks like this
- **Incremental:** Break down a project into smaller deliverable parts
- **Iterative:** Run through many development cycles in a circle until we've delivered what they want
![[Pasted image 20220315184453.png]]

#### Developmental Techniques
**Go ugly early:** First pattern to allow delivering of the highest risk features first allowing for early cut and run if it will fail

#### Advantages
**Responsive to Change:** Requirements for the iteration is gathered at its start so changes from the start of the project are caught
**Work Can Be Split:** Broken down into smaller parts so there is easier opportunity for simultaneous work
**Feedback:** Each iteration can be a deliverable so there is more opportunity to assess risk of failure

#### Disadvantages
**Budgeting is Difficult**
**Requirements for the iteration are up front:** Cannot respond to change inside an iteration so iterations must be kept small as possible
**Communication Problems:** Project is broken down which runs the risk of missed integration requirements or development not co-ordinated

#### When to Use
- Project is longer duration (1 iteration is commonly a month duration)
- There is more concern for a viable product than cost overruns
- Developer collaboration is difficult due to remote teams
- There is risk of requirements changing
- There are high risk features that may cause project failure

## Agile
- Umbrella term covering many formats of development
- Foundation is Iterative/Incremental design
- Assumption is your requirements are wrong and you will fail so let's fail faster, cleaner, and with less damage so we can fail again and still get it right by the end
- Trial and error until success

![[Pasted image 20220315190752.png]]

***Forms of Agile are about improving team communication and collaboration, getting a working feature in front of the requester as fast as possible so they can ask for changes. Iterations in Agile must be much faster. They will usually be contained in a major planning cycle called a Sprint. A slow Agile process will have weekly iterations with a monthly Sprint. The idea is each iteration has deployable/reviewable software at the end.***

![[Pasted image 20220315191008.png]]

#### Development Techniques
- The nature of Agile development brings a host of timeline and quality issues. To deal with them many of these techniques were developed and are usually required for an Agile team to be successful but they are not solely Agile practices. This is not an exhaustive list, just some of the more common.
	- **Scrum:** A prescribed set of work ownership and team communication structure. First step toward Agile. First step to the development team controlling what they work on.
	- **Lean:** Involves analyzing the team's throughput to production to find bottlenecks and improve efficiencies/eliminate waste. KANBAN is tied to this.
	- **Continuous Integration:** Developer checks in their change to a centralized source control and this automatically kicks off a release process for that code.
	- **Extreme Programming:** Combination of paired programming (2 people working on 1 computer to solve the problem) and procedural/functional programming. Idea based on developer spending 80% of their day solving and 20% coding. Applying 2 people to solving increasing coding throughput more than applying 2 people to coding and solving separately. Second based on Object Oriented Programming being too complex and that re-usability is a myth.
	- **Test Driven Development (TDD):** Writing an automated test first to drive the code that's written. Any further change is protected improving QA. (Deviations include Behaviour Driven Development, Acceptance Test Driven Development, Scenario Driven Development)

#### Advantages
**Responsive to Change
Work Can be Split
Business Priorities:** The business users usually control the order of work so developers are responding to highest needs

#### Disadvantages
**Budgeting is Difficult
Communication Problems:** Team has to be in nearly constant communication.

#### When to Use
- Project is longer duration
- There is more concern for a viable product than cost overruns
- Team communication is high and requesters are engaged
- There is a risk of requirements changing


# Software Requirements Specification

### Software projects should start with a specification!

- Specification can be in many formats depending on the templates favoured by the team you're in
- Some may be 20 pages long for a small project
- They can appear in a Functional Specification or a Software Requirements Specification.
	- **An Executive Summary:** This includes a summary of the business reason you're developing the features. All the features in the document should align to this summary. This is the business goal your team is trying to achieve.
	- **List of Features:** There should be a brief title and small description of each feature you will be working on. Likely a high-level description that may include a lot of functionality.
		- *Enter a Sale* - The users will enter the items for sale and take payment from the customer
			- What this means (these will appear as user stories or use cases)
				- Sales entry screen allowing entry
				- Product lookup and entry validation
				- Running total of sale
				- Applying discounts to sale
				- Payment processors
				- Saving the sale
				- Etc...
	- The Executive summary gives an idea of the projects purpose overall. The features give the list of Epics or major milestones. These then become the Use Cases and User Stories or if they are Epics are broken down into more cases the actor needs to do as part of that feature.

## Wireframing
- Wireframing helps clients understand what you will develop. It allows you to provide that tangible reference without developing which risks it being thrown away if requirements weren't understood.
- There are tools out there that allow you to create more advanced wireframes, to the point of having a clickable drawing on screen, but I find that a simple and quick drawing with a sit-down meeting provides as much return with far less setup. The idea is to present something to the user within minutes, if it will take days to do the wireframe then you might as well prototype instead.

## Use Case Detail
- A Use Case Detail document comes out of the waterfall style projects but ties to Object Oriented Development through a document language style called UML
- A Use Case details step by step how a type of user (actor) will interact with the system and what's expected of the system in return
- Analysts today separate Use Cases into two different types, one of them being System Use Cases

![[Coffee Use Case.jpg]]

## User Story
**Keys to a Good User Story**
1. Who will use it?
2. What would they like to do?
3. Why do they want it?
4. What must it do?

**Basic Common Structure**
- As a ***type of user indicated*** i want to ***perform a single sentence desired effect*** so that I ***an indicated business value***
	- The "So That I" section is often missed but without it, you will likely find the following:
		- The user has an idea, but no real understanding if it will be of use, investigation should be done or this will be unnecessary work
		- The user knows exactly what the end result should be and is dictating what they think the solution should be assuming you can't do anything else. Will cause a lot of re-work as you struggle to find what it is they are actually trying to solve.
	- The only thing missing from this is a clear **definition of done** so we add Acceptance Criteria, Constraints, and/or scenarios beneath when we talk to the requestor. This is where you have functional and non-functional requirements

- **Acceptance Criteria**: What will the users be testing on top of the simple sentence above to determine if the story is complete? (E.G. Must have a validation on screen if I don't enter this field.)
- **Constraints**: Are there limiting factors or outside concerns? (E.G. Must change the current sales process, Legal constraints, etc)
- **Scenarios**: How many ways can we see this happening? Are there different processes for different sets of data? Beware the words "I want it to always do this every time.

## Use Case Diagram
- Maps the use cases or stories that are needed to produce a system. It maps the case to the actor that will use it and maps the interactions between cases as well. An actor is the person, system, or time that initiates the use case and interacts directly with it. 
- A use case can interact with other use cases; a use case can either Extend another use case or Include it.
	- **Extend** - One use case may start from the other
	- **Include** - One use case always uses the other

![[Pasted image 20220330143355.png]]

- The developer is the actor, they want to make and drink coffee

![[Pasted image 20220330143425.png]]

- Some items in this process are needed only and always for making coffee, others could be used on their own, and some may be used by the coffee press or not. The Developer is still actively performing all actions, but they are now recognized to have relationships to each other. Note the additional arrows to include or extend now have specific directions.
	- Hot Water – Making Coffee requires this process (include)
	- Grind Beans – Making Coffee requires this process (pre-ground is not available currently) (include)
	- Brew - Making Coffee requires this process (include)
	- Cream – Nice to have if the Developer wants lighter coffee but not always required (extend)
	- Sugar – Nice to have if the Developer wants lighter coffee but not always required (extend)
- If we had a feature that coffee could be prepared the night before and an alarm would be set to brew the next morning. Then an additional actor of Time would interact with Brew alone.
