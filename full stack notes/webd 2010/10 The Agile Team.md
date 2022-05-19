---
class: webd 2010
module: module ten
date: 2022-04-27
tags: webd-2010 Agile agile-team agile-methodologies project-management
---

# Week 10: The Agile Team

### Agile Team
- The Agile Team can vary in terms of who is performing roles and responsibilities
- Some core tenants for success:
	- Co-location
	- Engaged (and ideally, available) customers
	- Self-organized
	- Accountable and Empowered
	- Cross Functional

### The Agile Customer
- They prioritize the features
- They make the important decisions
- They decide what gets built
- "The Source of Truth"

### The Agile Analyst
- Help write the user stories
- Does the detailed analysis
- Makes sure we've done our homework
- "I sweat the details"

### The Agile Teser
- Helps write tests for upcoming stories
- Confirms stories work as expected
- Thinks about the big testing picture
- "Because finding out in production isn't an option!"

### The Agile Project Manager
- Tracks how we are doing
- Communicates the state of the project
- Removes roadblocks standing in the team's way
- "Watching the bottom line"

### The Agile User Experience Designer (Sometimes the BA)
- Uses a collection of tools and techniques to help create a compelling user experience
- Overlaps with analysis
- Prototypes and concept designs
- "Because it's cool to think about the customer"

### BAs, Testers, and PMs in Agile
- For ***Business Analysts***, successfully managing an agile project depends on defining requirements in smaller increments and working more collaboratively with the team through the life of the project
- For ***Project Managers***, success moving to agile development methodologies depends on acquiring the skills necessary to progressively plan a project through its lifecycle rather than at the onset
- For ***Quality Testers***, evolving to an agile framework will mean develoiping the skills necessary to write tests and validate code in parallel with develoment

# Agile Development Methodologies
- Common Traits:
	- Frequent product releases
	- High levels of real time collab within the project team and customers
	- Reduced time intensive documentation
	- Regular, recurring assessments of value and risk to allow for change
- Not all Agile methodologies are iterative
- Not all iterative methodologies are Agile
- Agile is a subset of iterative development
	- Very common to blend methodologies based on:
		- Team composition
		- Skills
		- Experience
		- Operating environment

# Scrum
- One of the most predominant methodologies
- Work is performed in iterations -> sprints
	- Typically in between 2 to 4 weeks
- Each sprint must produce working software
	- Quality high enough it could be delivered to the customer or deployed

### The 3 Pillars of Scrum
1. **Transparency**: Give visibility to those responsible for the outcome
2. **Inspection**: Checks on how well a project is progressing towards its goals and looking for deviations
3. **Adaptation**: Adjusting a process to minimize further issues

### Ceremonies and Backlogs
- Four types of meetings called Ceremonies
	- Sprint Planning
	- Daily Scrum
	- Sprint Reviews
	- Sprint Retrospectives
- Product backlogs list all reqs
- Serves as wishlist for the project
	- Keeping track of all requests and prioritized within
- At the beginning of the sprint, the ***Spring Planning*** ceremony is held
	- Team reviews backlog and identifies highest priority items
	- High priority items move from **Product Backlog** to **Sprint Backlog**

### During a Sprint
- Team refines understanding of the contents within the Sprint Backlog
	- Detailed analysis is performed, acceptance criteria defined
		- Just in Time Requirements Gathering
- Team meets daily at Daily Scrum ceremony to review:
	- Work Completed
	- Work in Progress
	- Roadblocks
	- Scrum of Scrums - A technique to scale Scrum up to large groups(over a dozen people)
		- Divides the groups into Agile teams of 5-10, each sub team Daily Scrum
		- Designates one member as ambassador to participate in a daily meeting with ambassadors from other teams
- Team delivers working and tested software that meets all selected Spring Backlog items

### End of Sprint
- **Sprint Review**: Customer reviews the software
	- Typically demonstration and feedback is provided, sometimes User Acceptance Testing is performed
- **Sprint Retrospective**: Team meets to find ways to improve the products and project processes, business analysts look for feedback on the requirements how and when those requirements are provided in order to find ways to improve their processes
- Both may identify additional items that feed into the *Product Backlog*

### Scrum Process and Backlog Management

Product Backlog -> Sprint Backlog -> Sprints -> Shippable Product
- Backlog management is the primary method of handling both requirements prioritization and change management in most agile methods

### Scrum Roles and Responsibilities
- **Product Owner**
	- Responsible for maintaining the list of work to be performed
- **Scrum Master**
	- Responsible for managing the Scrum process and removing roadblocks
- **The Development Team**
	- Responsible for developing and delivering the product

# Extreme Programming (XP)
- Iterative in nature, providing small releases at end of iteration
- Primary focus on technical aspects of Agile software development
	- Developer focused, but a business analyst informally plays a role

### 5 Principles
1. **Simplicity**: Reduce complexity, extra features, and waste
2. **Communication**: Make sure the team knows what is expected of them and what others are working on
3. **Feedback**: Get impressions early, fail fast to get new information while there is still time to improve the product
4. **Courage**: To allow work to be entirely visible to others
5. **Respect**: That everyone works differently and is accountable for the success for failure of the project

### User Stories
- User Stories are XP's central mechanism to define reqs
- Created to define features and functionality to be included in the solution
	- User stories do not contain great detail and are used to: 
		- Prioritize work into iterations
		- Estimate the effort required to deliver the request
		- Establish a conversation between the team and the product owner around the subject of the real business needs, in order to create a common understanding of what has to be done
		- Identify acceptance criteria for requirements

### XP Planning
- ***Release Planning***
	- Identifies next step of usable features that make up a release
	- Contains one or more iterations
	- Release plan is similar to Sprint Backlog -> both focus on releasable software, Sprint Backlog is one iteration however
- ***Iteration Planning***
	- Work to be completed in each iteration that will allow a releasable product
- ***Daily Planning***
	- Daily activities to ensure team is on schedule and roadblock identification

### XP Roles and Responsibilities
- Customer: Creates and prioritizes the user stories and performs risk analysis
- Developer: Communicates directly with the customer and builds only what is necessary to deliver on each iteration
- Tracker: Keeps track of the schedule and metrics

### XP and Business Analysts
- While XP does focus on value drivewn development, it does not explicity address business analysis activities
	- Fundamental assumption the customer role is filled by a small number of people who know what the most valuable features will be
	- BAs add significant value facilitating larger scale projects or with customers who do not have a clear vision of the incremental value of features
	- BAs also contribute by facilitating story mapping
	- BAs perform story decomposition and story elaboration

### XP and Risks with the Customer Role and Requirements
- Risks with user stories created and managed directly by the user:
	- Requires training and experience in basic requirements gathering/documenting
	- Unfiltered requirements can constrain a solution
	- Still require more detail for acceptance criteria; most users won't be able to articulate without facilitation

### Scrum vs XP
| Scrum |    XP |
| --- | --- |
| All types of Projects | < 20 People |
| Customer Driven   | Customer Driven |
| Burndown Chart   | Task List |
| Product Backlog, Sprint Backlog   | Feature Cards |
| No Architecture Docs   | Architecture ModelClass-Responsibility-Collaboration (CRC) Cards |
| High-Level Models Prototyping   | SkecthesClass-Responsibility-Collaboration (CRC) Cards |

# Agile Business Analysis

## Kanban
- Methodology for managing the flow of work to allow for change
- Five key principles:
	- Visualize the work
	- Limit work in progress
	- Focus on flow
	- Make process policies explicit to team
	- Continually improve
- Does not require fixed iterations
	- Work moves through a continuous flow of activity
	- Team only works on a fixed number of items at any one time
	- Work may only begin on a new item when it is required to maintain flow downstream and the previous item is complete

### Kanban Queues
- Uses queues to control work in progress
- Take from the previous queue and move a new queue without skipping steps
- Ex:
	- Product Backlog (List of requests or change requests)
	- Waiting for Analysis
	- In Analysis
	- Waiting for Development
	- In Development
	- Waiting for Testing
	- In Testing
	- Ready for Implementation
	- Implemented
- Kanban is often combined with Scrum
	- Product Backlog can often be the first queue
- Also similar is the grooming of the queue
	- Periodic exercise where project team scopes the features waiting in the queue to see if they need to be decomposed into smaller chunks or are out of scope
	- Reassess priority of items in the queue
- As a measure of progress, Kanban measures "lead time"
	- How long did it take us to implement a feature from the moment it became a request on the Product Backlog?

### Kanban Board
- Visualize the work
- Kanban board is a visual depiction of the flow of work through the software development process
![[Pasted image 20220428150319.png]]
- Use different coloured stickies for:
	- Features and stories
		- Include brief description, date started, date finished, and priority
		- Must indicate who is working on it now
	- Defects
	- Tasks
- Find a way to visually indicate completed and blocked items

### Kanban Work in Progress Limits
- The team will agree on WIP limits per queue
	- Typically, more than one but the lower the better
- WIP consumes capital and delivers no return until work is completed
	- Represents money spent with no return, which we want to limit
- WIP hides bottlenecks in processes and masks efficiency issues
	- Less WIP, more visibility to issues
- Display and enforce WIP limits per queue

### Benefits of the Kanban Board
- Can often be the easiest Agile methodology to implement
- Project status at a glance
- Work in Progress Limits
- Clear expectations
- Easy to read

### Kanban Roles and Responsibilities
- No defined roles, the intent is to bring the team together by increasing communication and collaboration
- BAs identify new features in the backlog
- Requirements analysis is performed on the prioritized features
- Time estimates are provided for each activity

# Lean Software Development
- Agile Framework taken from Toyota
- Principles: 
	- Eliminate waste
	- Amplify learning
	- Decide as late as possible
	- Deliver as fast as possible
	- Empower the team
	- Build integrity
	- See the whole
- Focuses on flow or smoothness of work and minimizing waste

# Dynamic Systems Development (DSDM)
- Based on concepts of Raipid Application Development (RAD)
- Principles:
	- Focus on business need
	- Deliver on time
	- Collaborate
	- Never compromise quality
	- Build incrementally
	- Develop iteratively
	- Communicate continuously and clearly
	- Demonstrate control

