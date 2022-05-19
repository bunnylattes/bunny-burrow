---
class: webd 2010
module: module 14
date: 2022-04-29
tags: webd-2010 project-management Agile 
---

# Agile Planning

### Inception Deck
- A quick reminder about why we are here, who our customers are, and why we decided to do this project in the first place
- It's all about discovering your commander's intent and going and seeing for yourself

### Elevator Pitch
- A good elevator pitch will do a number of things for your project:
	- Brings Clarify: forces teams to answer tought questions about what the product is and who it's for
	- Brings focus into what the product does and why: teams gain valuable insight into what's compelling about the product and why their customers are buying it in the first place
	- It gets to the point: this clarity helps set priorities and greatly increases the signal to noise ratio of what really matters

#### Elevator Pitch Template
- For (target customer)
- Who (statement of need or opportunity)
- the (product name)
- is a (product category)
- that (key benefit, compelling reason to buy)
- unlike (primary competitive alternative)
- our product (statement of primary differentiation)

### Product Box
- Asking why someone would buy the product or service
	- Gets your team forucsed on what's compelling for your customer and the underlying benefits of your product
- Step 1: Brainstorm the product's benefits
- Step 2: Create a Slogan
- Step 3: Design the Box

### The "Not List"
- Create a Not List
- It's pretty clear what we do
- In Scope:
	- Create new permit
	- Update existing permits
	- Search
	- Basic Reporting
	- Print
- Out of Scope: 
	- Interfacing with legacy road closure system
	- Offline capability
- Unresolved:
	- Integration with logistics tracking
	- Security card swipe system

### Meet Your Neighbours
- Our project community is always bigger than we think, invite them over for coffee and introduce yourself and project

### Show Your Solution
- Determining what we are up against technically and gaining agreement on how we're going to build
	- Sets expectations around tools and tech
	- Visualizes assumptions around project boundaries and scope and communicates risk
- Valuable for assessing assumptions and initial gaps
- *Caution:* Use Iteration 0 for detailed solution architecture layer planning

### Inception Deck Risks
- Discuss some of the challenges you and the team might face when delivering and what you can do to prevent them from ever happening
- Talking about risk is good!

### Size It Up
- Involves looking at your estimates and coming up with a rough plan for your stakeholders
	- Including user acceptance testing UAT, training, and anything else
- Best guess at how big you think this thing is and whether it can be done in a reasonable period of time

### Trade Off Sliders
- No two can occupy the same level
- 1st four are the most important while the others contribute to whether the project will be viewed as a success
![[tradeoff.jpg]]

![[whatititake.jpg]]

### Assemble the Team
- Best if done after inception deck
- List quantity of roles and detail responsibilities
- Ensure everyone knows who is calling the shots (stakeholder prioritization)

# Strategic Planning
- Business capabilities for the current state and future state of an organization can be used to determine where that organization needs to go in order to accomplish their business strategy
- As a result of performing a business capability assessment, there is generally a set of recommendations or proposals for solutions that need to be put in place
- This info forms the basis of a product roadmap and serves as a guide for release planning
- Without a clear understanding of business value, it is possible for the project to deliver something that sounds valuable but isn't
- A project creates business value when it delivers anything that contributes to an organization's stated primary goals, for example:
	- Increasing or protecting revenue
	- Reducing or avoiding costs
	- Improving service
	- Meeting regulatory or social obligations
	- Implementing a marketing strategy
- Often projects create options for the business to exploit, for example the option to sell 1000 items of a product in a day
- Business value should be expressed in the form of a model rather than absolute amount
- The most important aspect of developing a business value model is the convo thatgenerates the shared understanding, rather than the model and the numbers
- Examples of bad business value statements are:
	- This enables straight thru processing
	- This will make x amt of money
	- This will save x amt of money
	- Some guy needs this project/product
		- None of these show alignment with the goals of the org

# Release Planning
- At the beginning of a project, the team will create a high level release plan
	- The team cannot possibly know everything up front so a detailed plan is not necessary
	- The release plan should address: 
		- The number and duration of the iterations
		- How many people or teams should be on the project
		- The number of releases
		- The value delivered in each release
		- The ship date for the releases
		![[releasecomp.jpg]]
	# Backlog, Releases, and Iterations
	![[backlogsdh.jpg]]

### Iterations
- How long should an iteration be?
	- Varies per project but no longer than 6-8 weeks
	- Could be as little as a few days or a week
	- The longer the iteration is, the less business value because you're not delivering things fast enough or failing fast enough
- How many iterations should there be?
	- Take your total master story list, 
- Remember to look at testing as an input
	- Are you automating?
	- What's regression tesing efforts going to look like?

### Prerequisites for Agile Execution
- A way of doing analysis that is light, that is accurate, and that gives exactly what you need, just when you need it
- Development practices will need to be rock soli
	- No time to continuously go back and fix buggy code, it has to work out of the gate
	- That means well designed, well tested, completely integrated code as you go
- Testing will have to be lockstep with development
	- Can't afford to wait until the end of the project to see whether everything works, you are going to have to maintain the health and integrity of the system from day one
![[iterationlife.jpg]]

### Waterfall vs Agile

![[waterfallvsagile.jpg]]

# Iteration 0
- In Agile, when do we perform the items that are necessary that the customer may not view as "value-added" features but need to be done?
	- Building/configuring hardware
	- Planning and configuring the solution architecture
	- Installing and configuring software on all environments
	- Setting up users/roles
	- User Interface Design
	- Version Control
	- Automated Build Process
	- Hello World Screen
- Iteration 0 is about getting our house in order, it's about setting up things and getting our development and test (and if we can, production) environments working so we have something to deploy against
	- Often includes a basic feature that goes end to end and tests the architecture
- Depending on how you look at it, iteration 0 is your first iteration or it's the iteration before you start
- If we were mid-project, we would normally just dive in and start doing the work on a given story after doing the analysis but if we are just starting a new project, there are certain things we'd like to have in place before
	- We call this setup phase iteration 0

### *Establish Domain Language Early*
- When the words used in your software don't match those used by the busines:
	- The wrong abstractions get built into the software (business will think location means one thing, developers another)
	- Software becomes harder to change
	- End up with more bugs and higher maintenance
- To avoid this, create a common language that you and the business share
	- Write them down
	- Clearly define the words
	- Match those definitions on the software
- Minimizes refactoring and makes easier to talk to customer

![[interation0.jpg]]

# Estimating
- In agile, we accept that our initial, high level estimates aren't to be trusted
- However, we also understand that budgets need to be created and expectations need to be set
- Need two things: 
	- Stories that are sized relatively to each other
	- A point based system to track progress
- *Do not make promises too early*
- Estimating is progressive and occurs in alignment with iterations
- No one expects early estimates to be accurate as later estimates
- User stories are typically estimated in story points
	- Story points can be abstract measurements that provide a numeric value to a story, or story points can be described as ideal developer days
	- A story point is a number assigned to each story that defines the estimated effort a team needs to complete the story
	- Story points are usually based on what the team knows about the story in 4 key areas
		- Knowledge
		- Complexity
		- Volume
		- Uncertainty

### Ambiguity Polls
- Donald Gause and Gerald Weinberg suggest using ambiguity polls to spot places where people disagree because of hidden assumptions and help them reach an agreement
- Consists of selecting a metric that requires a solid understanding of the domain estimate, this can be performance, cost, or time to complete a task
- The participants in the poll are asked to estimate the metric independently and then discuss the variations in results
- With a larger number of ppl, these polls often have clustered results where cluisters denote differences in understanding and variations in a cluster often relate to observational differences

### Story Point Estimating / Planning Poker
- Estimate as a team:
	- Customer reads story
	- Developers ask questions until finished
	- Developers write an estimate on a card in ideal X of work
	- Estimators turn them over
	- High and low explain estimates and assumptions used
	- Group discusses, customer clarifies
	- Re-estimate
- Another Explanation:
	- Team meets in presence of customer
	- Each team member holds a set of playing cards with numerical values for the points estimation of a user story
	- Customer briefly states intent and value of a story
	- Each member of the development team silently picks an estimate
	- When everyone has estimated, the cards are turned face up
- Offers an opportunity to leverage the knowledge of all team members
- Less structures meeting format
- The convo following the revealing of initial estimates is a great way to pool insights about the user story being discussed and surface implementation risks

### Why It Works
- The people stimating are the ones doing the work
- Planning poker isn't a voting system but a way to voice opinions and have better estimates

### Advantages
- Relative estimation is a simple, reliable method
- Highly adaptive and is likely to become increasingly accurate as time goes on
- Highly collaborative process based on consensus and likely have positive impact on team

### Disadvantages
- Relative estimates are based on historical data and accuracy is dependent upon the similarity of new stories to stories previously delivered, if new stories differ radically from previous, it is possible that the accuracy may decrease
- The accuracy of velocity is dependent on the knowledge and experience of the dev team, any changes to team will impact

# Spikes 
- If you run into something you've not done and don't know how to do it, do a spike
- A time boxed experiment where we do just enough investigation to come up with estimate
- Spikes are usually no more than a couple days and are a great way to try something out fast, get info, and provide an estimate

# Team Velocity
- Total number of story points within any given iteration is considered to be the team's velocity or how much a team can accomplish within an iteration
- After several iterations, teams will have better understanding of their velocity and will allow them to make better estimates
- Total Story Points for an Iteration
	- Try to level the points
	- Place dependencies or recs functionality before those requiring or desiring them
	- Retrospective, measure completed points against planned
	- Adjust iteration plan accordingly

# Triangulation
- Agile recommends freezing your estimates on a simple point based system and not typing them to elapsed time on the calendar
- So long as we size our stories similarly to each other, for every story we over estimate, there's another we under estimate
- Using a point based system:
	- Reminds us that our estimates are guesses
	- Measure of pure size
	- Fast, easy
- Taking a few sample reference stories and sizing our other stories relatively
- Ideally something small, medium, large enough to fit within one iteration
- Search for candidate stories to size against
	- Logical groupings
	- Stories that go end to end
	- Anything typical
- Resize outliers and give them a more realistic number
- By sizing our stories relatively to each other and measuring how fast we can go, we have all the ingredients to begin forming our agile plan