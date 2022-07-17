---
class: webd 2011
module:  module three
date:  2022-05-12
tags: term-2 webd2011 
---

# Creating a Service Layer

### Layered Pattern
- The first concept of separating code was with enterprise applications
- Separated classes by purpose into layers to make easier to find
- Separation into different projects or DLLs
- Client, Business Logic, Data Access were the layers (3Tier Architecture)

#### Client Server
- SOAP: Simple Object Access Protocol
- Client could build and use object the server understood, send that to the server via a webservice thgat would convert that object to an XML stream, and the server would receive it as a valid object that it understood
- nTier: multiple layers
- Client, Server, Business Logic, Data at the minimum

#### Microservice Architecture
- SOAP slow 
- Anti Patterns:
	- Easy to setup a new service in the existing service whenever a new request came in, this made API Monolith common
	- Increased coupling bc the client and server were using the same DLL, both had to be updated simultaneously to prevent versioning issues
- New pattern in old architecture: use less forced adherence and more as needed validation over the older HTTP calls directly
- Domain Driven Design introduced to create a new API for every context to decrease risk of API Monolith
- Client builds the parameter and the server manually translates data streams into objects, speeds up communication time and removed direct coupling
- HTTP calls are simple and straightforward (GET, POST, PUT, DELETE) and so is the pattern, making it easy for developer to implement an entirely new service as the contrext changed
- No dependency on large libraries and published WSDL files, easy to post your simple service to online servers like AWS
- Faster service, easily publishable near customer base with clouds