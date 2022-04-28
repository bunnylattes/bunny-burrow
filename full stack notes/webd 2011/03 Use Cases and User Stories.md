---
class:  webd-2011
module:  module two
date:  2022-03-15
tags:  #objectoriented #web-2011
---

# Use Cases and User Stories

### Use Cases

- **Title**: What is the goal?
- **Primary** **Actor**: Who desires it?
- **Success** **Scenario**: How is it accomplished?

#### Title
- Should be a short phrase with an active phrase that describes a goal
- A title could be "Heat Meal" 

#### Actor
- It could be a user or someone more specific like a customer or employee
- Any external entity that acts on the system

#### Scenario
- Paragraph Example:
	- Astronaut inserts meal package. System identifies type of meal. System heats package for length of time required for meal type. System notifies astronaut that meal is ready via space pager. Astronaut removes package from system.
- Steps Example:
	- 1. Astronaut inserts meal package
	- 2. System identifies type of meal
	- 3. System heats package for length of time required for meal type
	- 4. System notifies astronaut that meal is ready via space pager.
	- 5. Astronaut removes package from system.

**Extensions or additional details in the case of failure**
- Example:
	- 2a. Describe steps for unidentifiable package.
	- 4a. Describe steps for space-pager system error.

**Precondition**
- Astronaut has identified at least one meal to cook

**Fully Dressed Use Case**
- Contains Postconditions, Secondary Actors, Stakeholders, Scope, Priority, Owner
- Usually a PDF or Word template to fill in
- Try not to make it so complicated, it can kill progress.

***Further Reading: Writing Effective Use Cases by Alistair Cockburn***

### Identifying Actors
- Must brainstorm how many people and what kind of people will use the system or application
- Must brainstorm the possible other systems interacting with it
- Must identify the goals of the users
	- Example: astronauts heating the meal, mission control monitoring the meals (cooks and observers)
- When writing use cases, the primary actors aren't necessarily the most important, they are the ones who begin the process (the cooks, in this case)

### Identifying Scenarios
- Describe a goal the actor can accomplish in a single sentence
	- Turn on microwave (?)
	- Emphasize the user's intent and goal, so actually make it:
	- **Cook meal**
- Use Cases should focus on the true goal:
	- Order supplies
	- Generate reports
- Envision typical situations that would occur in the event of an error
- Use active voice: omit needless words
	- "Astronaut inserts meal package"
	- Avoid too much detail and programming language, do not write pseudo code
	- Do not describe the user interface

**Use Case Prompts**
- Who performs system admin?
- Who manages users and security?
- What happens if the system fails?
- Is anyone looking at performance metrics or logs?

### Diagramming Use Cases
- A Use Case Diagram is a diagram of several use cases and actors at the same time

1. List out the Use Cases: Heat meal, Generate reports, Change settings
2. Insert actors
3. Draw a box around all Use Cases to represent the system
4. Draw a line between actors and the Use Cases that apply

### User Stories
- Shorter and simpler than a Use Case
- One or two sentences commonly written on index cards
- Format: 
	- **As a *(type of user)* I want *(goal)* so that *(reason)***
	- As a nutritionist, I want to see what astronauts eat so I can monitor their diet
	- As an astronaut, I want to schedule when I heat my food, so it will be ready later
		- AVOID USER INTERFACE OR TECHNICAL INFORMATION

#### Jukebox Use Cases Challenge
- Write two Use Cases and two User Stories for the Jukebox

**Mine**

*First Use Case*
- Title: Play Music
- Primary Actor: Astronaut
- Scenario: Astronaut selects track, system plays the track

*Second Use Case*
- Title: Identify User
- Primary Actor: System
- Scenario: System identifies user

*User Stories*
- As an astronaut, I want to play music so I am entertained
- As an astronaut, I want to see various tracks so I don't get bored

**Solution**

*First Use Case*
- Title: Play a Song
- Primary Actor: User
- Scenario: System identifies user. User browses library of available albums. User selects an album and browses list of songs on the selected album. User selects a song. System plays the selected song.

*Second Use Case*
- Title: Select Multiple Songs
- Primary Actor: User
- Scenario: 
	1. System identifies user
	2. User browses available albums and songs
	3. User selects a song
	4. System begins playing selected song
	5. User continues browsing and selecs a second song
	6. System adds second song to play queue
	7. System plays second song after first song is over

*User Stories*
- As a user, I want my song to be added to the front of a long play queue, so that I don't have to wait hours to hear it.
- As a user, I want to be identified without touching anything, so that my hands are free to do other things.