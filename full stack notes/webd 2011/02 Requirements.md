---
class:  webd-2011
module:  module two
date:  2022-03-15
tags:  #objectoriented #web-2011
---

# Requirements

### When and why do we use OO languages?

#### Defining Requirements

- Requirements = what does it need to do? What does it NEED to do?
- Non-functional requirements = how should it be done?
	- Legal
	- Performance
	- Support
	- Security

#### Functional Requirements
- Use phrases like "the system must"
	- These things will define what HAS to happen in specific
	- Do not talk about languages when defining these requirements

#### Non-functional Requirements
- Describes characteristics and not features
- "The system should be/the application should be"

### FURPS Requirements
- Functionality: capability, reusability, security
- Usability: human factors, aesthetics, consistency, documentation
- Reliability: availability, failure rate & duration, predictability
- Performance: speed, efficiency, resource consumption, scalability
- Supportability: testability, extensibility, serviceability, configurability

#### FURPS +
- Design
- Implementation
- Interface
- Physical

***Further Reading: Software Requirements by Karl Wiegers, Mastering the Requirements Process by Suzanne and James Robertson***

#### Jukebox Requirements Challenge
**A space jukebox that runs without money but prevents one person capitalizing on it by having a sole pick jump ahead of the queue when the first person chooses three or more songs.**

***Functional Requirements***
- The system must accept picks without payment
- The system must not let one person choose more than three songs at once
- The system must play music

**Solution**
- Functionality: 
	- The system must
		- Maintain a library of albums and songs
		- Allow users to brows albums and songs
		- Allow users to select individual songs
		- Prevent users from playing full albums
		- Maintain a queue of songs to play
		- Play music
		- Allow users to sort by artist
		- Identify individual users
		- Track number of plays per user
- Non-Functional:
	- The system should
		- Be intuitive to use while floating in space
		- Available 24/7
		- Low-power
		- Updatable

***This isn't comprehensive this is a starting point***