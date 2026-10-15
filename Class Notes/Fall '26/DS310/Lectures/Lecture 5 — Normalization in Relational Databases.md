---
Date Created: 10/13/26
Kind: Lecture
Domain: Data Science
Last Updated: 10/13/26
State: "6"
Action: Study
---
__Database Normalization__: A hierarchical methodology of database structure constraints
- The main idea is to maintain data integrity through all processes
- *Normal Forms*:
	1. __First Normal Form__ (1NF): Most basic; everything is a relation, primarily enforced through relational algebraic rules (SQL)
		- *Constraints*:
			1. Only single values in every cell
			2. Single data type per column
			3. No repeated rows
		- ==🟢*Advantages*==
			- Simplified operations
			- Makes one-to-one relations possible
			- Flatness (no nested tables)
	2. __Second Normal Form__ (2NF): 1NF + All columns must depend on the *entire* primary key
		- Specific to composite attribute primary keys
	3. __Third Normal Form__ (3NF): 2NF + All columns depend on *only* the primary key
		- In other words, there cannot be any columns that indirectly depend on the primary key through another column
		- When dependencies arise, split tables
		- ==🟢Column edits wont break any hidden dependencies between rows==

__==🔴Relational Model Criticisms==__:
- Performance suffers especially for multiple-access tables (such in many-to-one relationships)
- Complex data structures translate poorly into relational constraints

