---
Created: 10/12/26
Kind: Lecture
Domain: Data Science
Last Updated: 10/12/26
State:
Action: Study
---


__Relational Model__: Coined by Edgar Codd in 1970; provided a then-revolutionary abstraction of data access and representation independent of its physical parts
- Important Concepts
	- *Functionally-Defined Terms*
		- __Database__: A collection of tables
			- Its *rows* represent an entity and data that describes it (attributes or relationships)
			- Its *columns* represent an attribute of an entity
		- __Table__: A relation
			- __Row__: A tuple
				- Each row must be unique (identical rows are considered duplicates)
			- __Column__: An attribute
				- *Requirements*:
					- Each column must have a unique name
					- Values within must be of the same type
					- Each cell must have a single value
		- __Relation Schema__: Must include the
			- Relation's name,
			- Attributes' names and domains
$$Relation\_Name(attribute\_names, ...)$$
			- __Relational Database Schema__: Consists of all the schemas of all the relations in the database
	- __Null__: Indicates unknown/undefined values
		- Most column domains include null as a value

__Converting an ER Diagram to Relational Database Schema__
- *Entity Set* $\rightarrow$ Relation with same attributes
- *Relationship Set* $\rightarrow$ Relation with same attributes, in addition to the primary key(s) of the connecting entity sets

