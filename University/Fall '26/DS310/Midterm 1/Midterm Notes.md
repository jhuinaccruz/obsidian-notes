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
	- __Relationships between Entities__ (Relationship Set): The collection of relationship between each entity in it (==🔵denoted using diamonds)==
		- May also have its own set of specifying attributes
		- The key of a relationship set may be formed by taking the union of the primary keys of the entity set(s) in the relationship
- __Constraints__:
	- __Cardinality__ (Key): Specifies how many times an entity can appear in a relationship set (==🔵denoted by arrows==)
		- *Many-to-One*: An entity in `A` is mapped to *at most one* entity in `B` $$A \rightarrow B$$
		- *One-to-One*: An entity in `A` is mapped to *at most one* entity in `B`, *and* vice versa $$A\leftrightarrow B$$
		- *Many-to-Many*: An entity in `A` is mapped to any arbitrary number of entities in `A`, or not at all $$A — B$$
	- __Participation__: Specifies an entity *must* appear at least once (==🔵denoted by bolding or doubling the line/arrow==)

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
- *Relationship Set* $\rightarrow$ Relation with primary key(s) of the connecting entity sets (unless otherwise specified)
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

__Subquery__: Allows for nesting of queries

__Steps for Writing Queries__:
1. Start with `FROM`
2. Determine join conditions (especially when working with multiple relations)
3. Determine if `GROUP BY` is necessary
4. Determine Other necessary conditions
	1. `HAVING` for aggregate functions
	2. `WHERE` for non-aggregate functions
	3. Subqueries?
5. `SELECT`/`ORDER BY`/`DISTINCT` for final presentation

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

__Hard Drive__: Persistent storage consisting of a divisible magnetic domain, oriented up or down to represent a single bit, spinning while a metal arm manipulates it (reading and writing) across it
- __Track__: A complete ring of a single plate at any given radial distance 
- __Block__: A smaller subdivision; the smallest that can be read/written at one time (typically between 4-8kB)
- Only respond to simple commands (`read/write ...)`

__Field__: Individual data value
__Record__: A group of fields
__Collection__: A group of records

__Pages__: The smallest unit by which the DBMS manages data
- May be larger than a block

__Metadata__: Data about data
- *Per-record*: Data about a single record
	- Used for fixed field length/number of fields
		- Use delimiter (`#`) when the length is less than allocated space
- *Per-collection*: Data about an entire collection of records
	- Use for variable field lengths, positional data, and record headers
		- Use offsets for record headers
			- ==🔵$\text{offset}_0$ is metadata offsets ($1 + $ number of metadata columns)==

>*We will make the following assumptions about data in the rest of the lecture*
>- *Rach character is stored using 1 byte*
>- *Integer data values are stored using 4 bytes – up to 4 billion*
>- *Integer metadata (e.g., offsets) are stored using 2 bytes – up to 65k*

__Disc Accessing__: The reading of a single block (or series of concurrent blocks as a page)
- The most time-consuming process due to the fact that seeking processes take the longest

__Index__ (Dictionary/Map): A structure that stores `key, value` pairings (as *items*)
- Allows for efficient access to a record
- Structures can be
	- __Clustered__ (Primary): Stores full records based on some primary key
		- Also called a heap file due to management similar to the heap
	- __Unclustered__ (Secondary): Enable for quick record retrieval of items within records

__B-Tree__: Search tree data structure characterized that functions like a binary search tree with multiple children per node
- *Definitions*:
	- *Order* (Height): $m$
	- *Nodes* (Leaves): At least $m$ and at most $2m$
		- For *internal nodes* (within its branches), at least $m+1$ and at most $2m+1$
		- Minima/Maxima ensure each block read gets *as much information as possible* while also ensuring information *does not exceed a given block*
		- Leaves and their pointers correspond to a specific page
	- *Root*: (Topmost node): As few as $1$ item
- Important Functions: Given an item with a key $k$
	- *Search*:
		1. Traverse through the root until you find an item that is greater than $k$
			- If $k$ is greatest, drop onto the n
	- *Insertion*:
		1. Search for $k$ through the tree until reaching a leaf node
			- If the leaf has less than $2m$ items, add item to the node
			- Otherwise, split the node
				1. Smallest $m$ items remain in the leaf
				2. Largest $m$ items drop down into a new leaf
				3. Middlemost item goes into previous leaf, acting as a pointer to the parent
	- *Deletion*: Given node $N$
		1. Search for the item and remove
			- If $N$ ends up with less than $m$ items:
				- If adjacent node has more than $m$ items, take some items and add it to $N$
				- Otherwise, merge with sibling
			- If $N$ is an internal node, do not remove it
				- Wait until the associated child node is merged later on
- Efficiency:
	- Traversal: $O(m + 1) \implies O(m)$ 
	- Search/Insertion: $O(\log_mn)$
- ==🟢Solves some of the deficiencies in Hash Tables==

__B+Tree__: Similar to B-Trees, except data items are only found in leaf nodes, and internal nodes contain keys and child pointers
- ==🟢Compared to B-Trees, B+Trees have more space for child pointers leading to shorter trees (and less disk read/writes)==

__Hashing__: Generalizes keys into integers, such that no matter the data type, the indices (keys) are all the same type
- __Hash Function__: Converts items into hash values (keys), ==🔵Denoted as some function $h(\text{item}) = k$==
- __Hash Table__: Index structure resulting from hashing items and their corresponding keys and pages
	- Stored as an array in memory
	- __Collision__: Two values hashed to the same value
		- Partially solved through buckets, but ==🔴must account for when the *bucket* is full==
	- *Efficiency*:
		- ==🟢Best==: $O(1)$
		- ==🔴Worst==: $O(k)$ where $k$ is the length of the largest bucket
	- ==🔴*Limitations*==:
		- Hard to create a reliable hash function
		- Unordered keys mean sorts and. range/rank searches are difficult
- __Static Hashing__: Number of buckets remains constant, instead relying on "overflow" buckets
	- ==🔴Overflow bucket access requires extra disk read==
- __Dynamic Hashing__: Number of buckets fluxuates as items increase and buckets fill
	- ==🔴Can result in large space expenses==
	- *Simple Approach*: Assuming keys are strings, take their length and use modulo to get a valid bucket number $$\text{bucket index} = h(k) \% \text{number of buckets}$$
		- If hash table fills up, *double the number of buckets and rehash all items*
- __Linear Hashing__: Hash value is a binary number read as $i$-rightmost bits and placed in its corresponding bucket $$\text{bucket index} = i = \text{ceiling}(log_2n)$$
	- If bucket index does not exist, *subtract by one*
	- *Important metadata*:
		- $n$: Number of buckets
		- $i$: Number of bits used to assign keys to buckets
		- $f$: Value of how full the buckets are
	- When $f$ is exceeded, add one more bucket, and update $n$ and $i$ as necessary
		- *Rehash the previous bucket index*

__Working Set__: Frequently accessed pages stored in cache

__Choosing an Index Structure__

| B/B+Tree                                                                                                 | Hash Table                          |
| -------------------------------------------------------------------------------------------------------- | ----------------------------------- |
| Working set fits in memory                                                                               | Working set is large and spread out |
| Working set is local (queries result in searches close to each other) (e.g. rank/count/range operations) |                                     |
>*Query processing and optimization is the part of the DBMS that sits between these two layers. It is responsible for taking a user query (in SQL) and executing it efficiently on the contents of the database.*

__Query Processing__: Extracting data from a database through
- Parsing and translating commands
- Optimizing command execution techniques
- Evaluating and choosing how to execute the parsed command

- DBMS stores for any given relation $r$:
	- $n_r$: Number of records
	- $b_r$: Number of blocks
	- $f_r$: Records per Block (Blocking Factor)
	- $l_r$: Record size
	- $V(A, r)$: Number of distinct values in given attribute $A$

__Evaluation Primitive__: Relational algebra operation annotated with instructions

__Query Plan__: A sequence of evaluation primitives
- 
- *Optimization* is evaluated as the best query plan with the *lowest cost*

__Query Cost__: Measured through how many blocks are touched
- __Standard Query Cost Function__: Given $b$ transfers and $S$ seeks $$C = b \times t_t + S \times t_s $$
	- where
		- $t_T$/$t_S$: Time per block transfer/seek
		- *Sequential Read*: One seek + $n$ transfers
		- *Scattered Read*: $n$ seeks + $n$ transfers

__Selection Algorithms__: Fundamentally always include some kind of file scan or index walk
- The specific combination depends on the kind of indexing and the condition by which data is read
- *File Scan*: $C = b_r + 1t_s$
	- Equality of keys: $C = b_r / 2$
	- Equality of values: $C = b_r$
- *Clustering* (B+Trees): $C = (h + 1) \times t_T + 1t_S$
	- ==🔴At small sizes, efficiency isn't improved over scanning== but ==🟢comparatively extremely efficient at larger sizes==

__Join Algorithms__:
- *Brute Force* (Nested-Loop): Process items per item (constantly switch between blocks) $C = n_r \times b_s. + b_r$
	- $r/s$: Inner/Outer
	- *Block Nested-Loops*: Process items per block rather than per item $C = b_r \times b_s + b_r$
		- Use smaller relation as the outer relation
- *Indexed Nested-Loop*: Using B+Tree's index search within a for loop; $C = (h + 1) \times b_r + n_r$
	- $h + 1 = c$ where $c$ is an estimate from the optimizing engine
	- Join should occur in order of most restrictive relation (in other words the relation with least rows)

__Cost-Based Optimization__:
 1. Denote equivalent expressions (based on *equivalence rules*)
 2. Annotate equivalent expressions with potential algorithms
 3. Estimate resulting plans using *statistics*
	 1. __Statistics__: Metadata that is used to estimate algorithmic costs
		 1. *Selection Size Estimate*: $\sigma_{A = v} / V(A, r)$
		 2. *Join Size Estimate*: $n_r \times n_s / max(V(A, r), V(A, s))$
 4. Choose cheapest step

__Equivalence Rules__: Determine two expressions produce the same result in *every* instance

>*Query processing and optimization is the part of the DBMS that sits between these two layers. It is responsible for taking a user query (in SQL) and executing it efficiently on the contents of the database.*

__Query Processing__: Extracting data from a database through
- Parsing and translating commands
- Optimizing command execution techniques
- Evaluating and choosing how to execute the parsed command

- DBMS stores for any given relation $r$:
	- $n_r$: Number of records
	- $b_r$: Number of blocks
	- $f_r$: Records per Block (Blocking Factor)
	- $l_r$: Record size
	- $V(A, r)$: Number of distinct values in given attribute $A$

__Evaluation Primitive__: Relational algebra operation annotated with instructions

__Query Plan__: A sequence of evaluation primitives
- 
- *Optimization* is evaluated as the best query plan with the *lowest cost*

__Query Cost__: Measured through how many blocks are touched
- __Standard Query Cost Function__: Given $b$ transfers and $S$ seeks $$C = b \times t_t + S \times t_s $$
	- where
		- $t_T$/$t_S$: Time per block transfer/seek
		- *Sequential Read*: One seek + $n$ transfers
		- *Scattered Read*: $n$ seeks + $n$ transfers

__Selection Algorithms__: Fundamentally always include some kind of file scan or index walk
- The specific combination depends on the kind of indexing and the condition by which data is read
- *File Scan*: $C = b_r + 1t_s$
	- Equality of keys: $C = b_r / 2$
	- Equality of values: $C = b_r$
- *Clustering* (B+Trees): $C = (h + 1) \times t_T + 1t_S$
	- ==🔴At small sizes, efficiency isn't improved over scanning== but ==🟢comparatively extremely efficient at larger sizes==

__Join Algorithms__:
- *Brute Force* (Nested-Loop): Process items per item (constantly switch between blocks) $C = n_r \times b_s. + b_r$
	- $r/s$: Inner/Outer
	- *Block Nested-Loops*: Process items per block rather than per item $C = b_r \times b_s + b_r$
		- Use smaller relation as the outer relation
- *Indexed Nested-Loop*: Using B+Tree's index search within a for loop; $C = (h + 1) \times b_r + n_r$
	- $h + 1 = c$ where $c$ is an estimate from the optimizing engine
	- Join should occur in order of most restrictive relation (in other words the relation with least rows)

__Cost-Based Optimization__:
 1. Denote equivalent expressions (based on *equivalence rules*)
 2. Annotate equivalent expressions with potential algorithms
 3. Estimate resulting plans using *statistics*
	 1. __Statistics__: Metadata that is used to estimate algorithmic costs
		 1. *Selection Size Estimate*: $\sigma_{A = v} / V(A, r)$
		 2. *Join Size Estimate*: $n_r \times n_s / max(V(A, r), V(A, s))$
 4. Choose cheapest step

__Equivalence Rules__: Determine two expressions produce the same result in *every* instance

__Transaction__ ==🔵(`txn`)==: Sequence of operations treated as a single operation
- *Characteristics* (__ACID__):
	- *Atomicity* (All-or-Nothing): All transaction's changes take place or none of them do
		- Perform an operation(s), then either
			- *Commit*: Changes are implemented and permanent
			- *Roll Back*/*Abort*: Changes are deleted, state remains as it was
	- *Consistency*: Changes (once committed) are consistent with database schema constraints
	- *Isolation*: Unaffected by concurrent transactions through *scheduling* (order of operations)
	- *Durable*: Failures do not affect committed changes
		- __Recoverable__: When a crash occurs between a commit, but the rollback affects a data value within the scope of the *current transaction only*
- ==🟢Prevents failed or overlapping operations from affecting the entire database==

__Concurrency__: Multiple processes running on a CPU accessing the same data
- Optimal concurrency relies on serializable, recoverable, and cascadeless transactions
	- Enforcing optimal concurrency requires its own management mechanism (e.g. *locking*)

__Parallelism__: Multiple CPUs running processes and accessing the same data

>*To address atomicity and durability, we incorporate a part of the system that performs logging and recovery.*

__Logging and Recovery Subsystem__: Revert changes to the last commit's version when transactions fail

__Schedule__: The order of operations for any given transaction(s)
- Conventional abstract notation is a series of read/writes in a table
	- Each column is a single transaction, where operations are performed in order of top to bottom, left to right. Additionally, can be denoted in shorthand as (for a given transaction $T_i$ and data $A$) $$r_i(A),\ w_i(A)$$
		- where $r/w$ denote read/write functions
- Can be divided into
	- __Serial Schedule__: One transaction *in its entirety* before the next one
- __Serializability__: The quality of being able to convert itself (a serial schedule) into a non-serial schedule with the same end results
- __Conflict Serializability__: The quality of being able to convert itself (a non-serial schedule) into a serial schedule through swapping non-conflicting actions
	- Conflicting actions act as *constraints* (one transaction must come before the other) for conflict serializability
		- __Precedence Graph__: Tests for conflict seriability (cycles = contradictions $\implies$ Not conflict seriable)
			- *Nodes* are transactions, and edges denote precedence constraints
		- ==🟢Easier to enforce than pure serializability==
- __Conflict__: When two actions cannot be swapped in order without changing the outcome of subsequent transaction(s)
	- Occurs when trying at least one transaction is trying to write over the same data value

>*all conflict serializable schedules are serializable...not all serializable schedules are conflict serializable*

__Dirty Data__: Data written by an uncommitted transaction
- __Dirty Read__: Read dirty data
	- Leads to cascading rollbacks (*avalanches*)

__Locking__: Provides a form of concurrency control through the control and giving of "locks" (data that allows a transaction to read/write)
- Pages, records, and even collections can be locked
- *Locks enforce serializability*
- __Two-Phase Locking__ (2PL): All locks must be acquired before releasing any
	- Enforce *conflict serializability*
- 