---
class: webd 2010
module: module 14
date: 2022-04-28
tags: webd-2010 project-management Agile 
---

# Agile Documentation: Story Planning Workshops

### Story Planning Workshops
- The goal of the story planning workshop is breadth
- Cast your net wide and discover as many features as possible to get everything on the table to have the big picture
	- When extracting user stories, look for small, discrete, end to end pieces of functionality
	- Usually one to five days worth of effort
- Epics are big stories that take a couple weeks of work
	- Handy for high level planning
- 10-40 high level stories are usually enough for 3-6 months of planning

![[uscase.jpg]]

#### Documentation
- If what you are doing is really complex and requires more time, do whatever it takes to elaborate on the requirements, however don't go so far ahead that you end up having to throw it all away because of how much things have changed
- Flowcharts are great because in a simple, visible way, they show how systems work
	- Show the steps people need to go through and gain some insight and understanding into who the users of your system are

# Story Mapping
- Provides a visual and physical view of the sequence of activities to be supported by a solution
	- Two dimensional grid structure
	- Horizontal axis: Walking Skeleton, sequence and groupings of key aspects of the product
	- Vertical axis: Detail and priority of stories
- Assists in creating understanding of product functionality, the flow of usage, and to assist with prioritizing product delivery (such as release planning)
- Used to visualize a product's requests in the context of usage and priority
	- Often placed on display for the project team during release planning sessions so the team can more readily identify dependencies generated as a result of the intended flow through the user stories

![[mapping.jpg]]
- The *Backbone* is what we need to build the system
- The *Walking Skeleton* represents a tiny implementation of the system that performs a small, core chunk of end to end working software

#### Developing Walking Skeleton
![[skelenton.jpg]]

### Advantages
- Good for identifying the larger context of a product
- Without it, agile projects can be subject to getting mired in the details with an inability to effectively string components together to create end to end business value
- Story mapping helps avoid the common problem of getting lost in the detail of the user stories and the risk of losing the big picture context

### Disadvantages
- Story mapping can become cumbersome where the product is very large and may require building a number of story maps that cover a large program of work
- Do not analyze or illustrate dependencies between requirements

# Story Decomposition
- Similar to existing requirements analysis techniques such as functional decomposition
- Provides a structure for defining the various elements of requirements at progressively smaller levels of granularity
- The most common agile approach to story decomposition can be described as breadth before depth
	- Start with a high level picture of business goals, decompose those into smaller components that provide increments of valuable functionality (minimally marketable feature sets or MMFs), split the components into user stories, and eventually elaborate the user stories with acceptance criteria
- A story that is too large or insufficiently understood to elaborate, estimate, or deliver as a story is an epic

![[decompo.jpg]]
![[decompo2.jpg]]
- Break up your features, epics, user stories, to what makes sense for your project and organization, there is no single right way

### Advantages
- Helps avoid common problem of getting lost in the details
- Able to trace implemented or requested functionality back to the driving business objectives
- Breaking the product into MMFs and epics helps with release level planning, provides visibility into the development project, and helps coordinate external program activities such as organizational change management and user training

### Disadvantages
- Need to avoid the temptation to treat story decomposition as a way of reverting to detailed requirements up front
- Ensuring the continued emphasis on just enough and just in time means knowing when to stop decomposing

# Story Elaboration
- Defines the detailed design and acceptance criteria for a user story on just in time, just enough basis
	- Lowest level of a story decomposition and the process by which the story sentence is into broken down into pieces of work
	- Done by someone on the team who has strong BA skills, particularly with facilitation and communication
- The result of story elaboration is a shared understanding among the participants of what the story means and what should be delivered to achieve done status
	- Detailed reqs for upcoming release
	- Task definitions and breakdowns
	- Examples and scenarios that explain the intent for the story
	- Low fidelity models that clarify the technical or process design
	- Screen or report mocups
	- Acceptance criteria (test design specs) to clarify how the story will be tested (given and when then)

### Advantages
- Avoids wasteful requirements elicitation and potentially documentation
- Avoids the work of eliciting reqs for features that may never be built or that will need to be changed

### Disadvantages
- Can be difficult to determine the best timing for conducting a story elaboration
	- Too early, the info may no longer be correct
	- Too late, it can delay project team progression to development
- Ability to elicit the appropriate level of detail such that the requirements can be developed, tested, to acceptance criteria

# Summary of User Story Usage

**User Stories:** Identify which roles the story provides value and therefore identify the stakeholders who can elaborate on that value, we determine what function those roles want and why

**Story Mapping:** Story maps show relationships between user stories and larger activities that the user must be able to accomplish

**Story Decomposition:** Epics, features, or minimally marketable features (MMFs) tie groups of user stories together into larger packages that can be discussed with stakeholders

**Story Elaboration:** Defines the detailed design and acceptance criteria for a user story on a just in time/just enough basis

# Use Case
- A method for designing information systems by breaking down requirements into user functions
- Each use case is a transaction or sequence of events performed by the user
	- Focuses on input and outputs of each actor, action, and system response
	- Help uncover requirements
	- Indicates to developers what the system must do and when

### High Level Content
- Activities that the system performs based on a user request or event, the activities are grouped by process
- A process should be clearly defined and not too large i.e. Create Order, Inquire on Order, Cancel Order
- Each step is written like a user scenario or story:
	- Actor action
	- System response
- Typically written in conjunction with business requirements and system specs
- Use Cases focus on what should be done not how

### Use Case Key Benefits
- Written in a language easily understood by the end user
- Helps define all the actors involved in a set of activities within a system
- Indicates reaction of the system per user initiated action
- Helps provide a sequence of related operations a system performs including error management
- Important in ensuring interactions are not overlooked

### Typical Use Case Contents
- Description/Purpose
- Priority
- Actors and Relationships
- Business Info
	- Activity Diagram, Class Concept Diagram, Text Description
- Business Rules, Requirements, Constraints
- Pre-Conditions and Post Conditions
- Trigger and Basic Flow
- Alternate Flow
- Usage
- Non Functional Requirements

![[usecaseex.jpg]]![[usecaseex2.jpg]]

### Alternate Flows
- Can use some of the basic flow steps
	- Alternate Flow begins after Step 2 of basic, etc
	- Alternate Flow inherits basic flow assumption and pre conditions
- List only the assumptions, pre conditions and post conditions specific to that alternate flow
- No limit as to how many alternate flows can be created for a use case
- Watch for "or", "if", or "then" when describing an actor's activity, it's often an indication of an alternate flow

![[differencess.jpg]]