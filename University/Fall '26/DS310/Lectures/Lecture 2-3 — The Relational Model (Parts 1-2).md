---
Created: 10/12/26
Kind: Lecture
Domain: Data Science
Last Updated: 10/13/26
State: "4"
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
	- Gets the same primary key
- *Relationship Set* $\rightarrow$ Relation with same attributes, in addition to the primary key(s) of the connecting entity sets
	- Primary Key transference depends on cardinality
		- *Many-To-Many*: Relationship Set Relation gets the *union* of the primary keys of the connected entity set(s)
		- *Many-to-One*: Assuming the relationship set exists, the primary key transfers from the *many* entity set
		- *One-To-One*: Assuming the relationship set exists, the primary key can be *either* of the connected entities'
- Special Cases (*Eliminating Relationship Set Relation(s)*):
	- *Many-To-One Relations*: Transfer attributes to the *many* entity relation
		- ==🟢Makes certain queries more efficiently executed and generally uses less space==
		- ==🔴May require a relationship nonetheless when the *one* side doesn't participate often in the relation (e.g. many null values)==
	- *One-To-One*: Transfer attributes to either entity relation(s)

>*For many-to-many relationship sets, we need to use a separate relation for the relationship set*

__Foreign Key__: Attributes in one relation that reference primary key values in another relation
- __Reference Integrity__: All foreign keys must match the values of the references attributes in another relation

__Relational Algebra__: A readable query language for denoting operations on relations, where each operation takes in as an input at least one relation and returns a relation
- Relations are treated as sets, and as such automatically remove duplicate tuples from the result
- Its operations include
	- __Selection__: Select tuples (rows) based off of matching a conditional $$\sigma_{\text{predicate}}(R)$$
	- __Projection__: Selects attributes (columns) from a relation $$\pi_{\text{attributes}}(R)$$
	- __Cartesian Product__: Combines two relations, such that the result is a relation with all possible combinations of tuples from both relations $$R_1\times R_2$$
		- In other words, combines attributes from both relations per tuple
	- __Rename__: Renames a relation (and optionally its attributes)
		- Just the relation: $$\rho_{\text{new\_relation\_name}}(\text{old\_relation})$$
		- Relation + Attributes: $$\rho_{\text{new\_relation\_name(attribute\_1\_name, attribute\_2\_name, ...)}}(\text{old\_relation})$$
	- __Natural Join__: Similar to Cartesian Product, except the rows are joined when their corresponding equivalents have the same value(s)$$R_1 \bowtie R_2$$
		- When no columns are shared between the two, then $R_1 \bowtie R_2 \iff R_1 \times R_2$
	- __Condition Join__: Similar to Cartesian Product, where the rows are joined based on the satisfaction of a conditional $$R_1 \bowtie_{\theta} R_2$$
		- where $\theta$ is the conditional/predicate
	- __Outer Join__: A Natural Join, in addition to extra rows for every tuple in a relation with no match in the other
		- *Left*: Extra rows for unmatched rows from the left (to the right) $$R_1 ⟕ R_2$$
		- *Right*: Extra rows for unmatched rows from the right (to the left) $$R_1 ⟖ R_2$$
		- *Full*: Extra rows for unmatched rows from either side to the other $$R_1 ⟗ R_2$$
	- __Set Difference__: Returns a relation of all the unshared tuples between them $$R_1 - R_2$$
	- __Assignment__: Gives a variable the result of an existing relation $$Relation\_name \leftarrow \text{relational algebra expression}$$
__SQL__ (Structured Query Language): The standard for querying most RDBMSs
- Relational Algebra Translations:
	- `FROM ...`: *Cartesian Product* of the selected columns
	- `WHERE ...`: *Selection* with the specified conditional(s)
		- When a conditional compares two columns of two different relations, it becomes a *join condition*
	- `SELECT ...`: *Projection* of specified attributes