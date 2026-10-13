---
Created: 10/12/26
Kind: Lecture
Domain: Data Science
Last Updated: 10/12/26
State: "6"
Action: Study
---
__Database__: Collection of related data
- __Database Management System__: Abstraction of software that controls the hardware and software components of a database
	- *Conventional Methodology*: Implement the *relational model* through SQL and a client-server model (server manages data, applications act as clients)
		- ==🟢Advantages==:
			- Allows for arbitrary queries
			- Consistent and reliable
		- ==🔴Disadvantages==:
			- Overkill for smaller projects
			- Expensive and difficult to manage
				- Difficult/impossible to implement on smaller systems
			- Limited functionality
			- Unnecessarily slow for some tasks
			- Limited scalability for clustering (nested databases)
	- *Two-Layer*: Subdivide *storage* and *logical* layers
		- *Storage Engine*: Controls and manages physical representation of data
			- Important aspects of the engine include the choice
				- Storage and index structures
				- Transaction representation(s)
				- Concurrency control
				- Logging and recovery
				- Distribution of Databases and Replications
		- *Logical Layer*: Manages abstraction of data (based off a given model) through query language tool(s)
			- Examples include
				- *Entity-Relationship Model*
				- *Relational Model*
					- SQL
				- *Semi-Structured Model*
					- XML
					  JSON
				- *non-relational SQL*

__Designing a database requires determining__:
- What data to include
- How data is related to one another and its groupings/decomposition

__Logical Schema__: Abstract description of the contents and structure of a database

__Entity-Relationship Model__: A visual non-implementational database design tool; specifies domain/scope of the items within and the relations between them
- *Components*
	- __Entity__: A single item/value ==🔵(denoted as a red rectangle)==
		- __Entity Set__: A collection of entities
	- __Attributes__: Describe an entity ==🔵(denoted as blue oval(s))==
		- ==🔵Double ovals represent an attribute that can have multiple values==
	- __Key__: Attribute(s) that uniquely identify each entity in its corresponding set
		- An entity set may have more than one possible key
		- __Candidate Key__: A minimal collection of attributes that constitute a key
			- In other words, a set of attributes such that removing any one of them from their corresponding key set makes the set not a key
			- __Primary Key__: Any candidate key chosen (==🔵denoted by underlining==)
	- __Relationships between Entities__ (Relationship Set): The collection of relationship between each entity in it (==🔵denoted using diamonds)
		- May also have its own set of specifying attributes
		- The key of a relationship set may be formed by taking the union of the primary keys of the entity set(s) in the relationship
- __Constraints__:
	- __Cardinality__ (Key): Specifies how many times an entity can appear in a relationship set (==🔵denoted by arrows)
		- *Many-to-One*: An entity in `A` is mapped to *at most one* entity in `B` $$A \rightarrow B$$
		- *One-to-One*: An entity in `A` is mapped to *at most one* entity in `B`, *and* vice versa $$A\leftrightarrow B$$
		- *Many-to-Many*: An entity in `A` is mapped to any arbitrary number of entities in `A`, or not at all $$A — B$$
	- __Participation__: Specifies an entity *must* appear at least once (==🔵denoted by bolding or doubling the line/arrow==)