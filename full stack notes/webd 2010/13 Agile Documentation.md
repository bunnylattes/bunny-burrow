---
class: webd 2010
module: module 13
date: 2022-04-28
tags: webd-2010 project-management Agile 
---

# Agile Documentation Backlogs and User Stories

### Low-Fidelity Artifacts vs. Long-Lived Artifacts
- Low-fidelity artifacts such as diagrams, maps, and lists provide more value to an agile project than long, textual requirement descriptions or specifications
- Developed for the sole purpose of building the software for a specific iteration
	- Only need to be intelligble to the team during the course of the iteration
	- Enable business value by creating context and generating shared understanding
	- Do not replace, or even take precedence over effective collabs and convos
- Long lived artifacts are intended to be utilized beyong the scope of development
	- May include the business case, charter, and documentation that is used to communicate what the software does and why it does it
- In the agile environment, understanding perspectives alongside the ability to hold successful conversations replace the need for formal, detailed, long term artifacts such as requirement documents

### Low Fidelity vs Long Lives Artifacts

![[low.jpg]]
# Backlog
- A list of features or technical tasks which the team maintains and are known to be necessary and sufficient to complete a project or a release
	- If an item on the backlog does not contribute to the project's goal, it should be removed
	- If at any time a task or feature becomes known that is considered necessary to the project, it should be added to the backlog
- The backlog is the primary point of entry for knowledge about requirements
	- The single authoritative source defining the work to be done
- There is not mandated format

### What is Included in Backlog?
- Backlog Items (aka Product Backlog Items)
	- Represent work to be done and convey customer thinking or tasks to reduce project risk
		- Prototypes, user stories, use cases, minimal marketable features, features, epics, or work item (defects)
		- Spikes
		- Tasks
- The incremental nature of the backlog allows new, higher value items discovered to enter into the existing backlog ahead of existing items
	- Shortens time to value

### Backlog Management
- The backlog is a fluid document that evolves over the course of the project as more is learned
- Product owner is responsible for ordering the items in the backlog based on business value, feature importance, or other relevant criteria
- When managing (or grooming) the backlog, items should be ordered so most important items are at the top
- During planning sessions, items are selected from the backlog based on factors such as priority, risk, value to the product or customer, and ability to deliver

#### Prioritization 
- Items in the backlog are ordered relative to each other
- Ordering can be established using numbering, value points, etc

#### Managing Changes to the Backlog
- Main mechanism for both managing change to the reqs on an agile project and controlling scope
- When new or changed reqs are identified, add to the backlog
- When an item is developed and accepted, the item is removed
- Product owner is responsible for managing the backlog, adding and ordering items, removing completed items, and revising the order on an ongoing basis

### Advantages
- Since the reqs on the backlog are ordered in importance, the team knows that what they're working on in a given iteration is high priority
- Those responsible for detailing the reqs review the backlog and determine if the items that will be developed in an upcoming release require further analysis in order to ready them for development
- Requirements are analyzed in detail on a just in time basis

### Disadvantages
- Large backlogs difficult to manage breaking the overall product backlog into backlogs for releases (called release backlogs) can help address this
- A lack of detail in the stories can result in lost info

# User Stories
- A lightweight requirements documentation method for shared understanding vs shared documentation
- Heavy documentation as a means of capturing reqs has never worked for software projects
	- Customers seldom get what they want
	- Teams seldom build what is needed
- As a **type of user**, I want **some goal** so that **some reason**
- Three essential aspects of user stories called *card, conversation, and confirmation*
- *Card:* User stories should be written on small index cards, the card allows you to write down only so much info so it cannot be a complete requirement
- *Conversation:* Where we flush out all the details and get to real requirements
- *Confirmation:* Each user story should be verifiable and we should have a clean way of deciding whether it was implemented correctly and completely

### Card
- Short descriptions of features
- We don't know at this point when we are going to get that feature or whether we will need it so we do not write a full requirement

### Conversation
- The problem with gathering reqs as documentation isn't one of volume, it's communication
- Written language is imperfect and subject to the decoder's interpretation

### Confirmation
- We want the aspects of our requirements to be measurable (testable)
- Need to articulate in small, verifiable chunks
	- Allow regular logins
	- Re-direct expired logins
	- Display appropriate error message
	- Handle non-existent user 

### INVEST Acronym
- **Independent**
	- Avoid interdependent stories
	- Prioritization and priority problems
- **Negotiable**
	- Details ironed out during convo
- **Valuable**
	- Must be valuable to the user
- **Estimatable**
	- Must be able to determine how much time it takes
		- 3 reasons why you cannot (Developers lack domain knowledge, developers lack technical knowledge, story is too big)
- **Small**
	- Must be right sized
	- Epics fall into two types
		- Compound stories
		- Complex stories
- **Textable**
	- Must be measurable

### Role Modeling
- User Roles
	- A collection of defining attributes that characterize a population of users and their intended interactions with the system
- Brainstorm initial set of roles
- Organize the initial set
- Consolidate the roles
- Refine the roles

*Tips*
- If there is a technical element to a user story, write in terms that the business can be excited about (provides business value)
- Turn solution constraints into system wide requirements or Constraint Cards if required
- Start with "Goal Stories"
	- Find a job brings about:
		- Search for a job
		- Subscribe to job alerts
		- Make resume available
- Closed Stories
	- Give the user a sense of accomplishing something discrete
- Constraint Cards
	- Include detailed solution constraints for the system where applicable
		- Date format, etc
- Keep the UI out as long as possible
- Ensure proper User Role context is the story
- Don't number
- Don't forget the purpose

#### How and When to Design UI
- Iteration 0
	- Up front UI design/guidelines
- Or,,
	- Perform user role modelling
	- Trawl for high level user stories
	- Prioritize stories
	- Refine high and medium priority stories
	- Organize stories into groups
	- Create paper prototype
	- Refine the prototype
	- Program

![[pro.jpg]]

#### User Stories vs. Other Requirements or Specification Documents
![[users.jpg]]
