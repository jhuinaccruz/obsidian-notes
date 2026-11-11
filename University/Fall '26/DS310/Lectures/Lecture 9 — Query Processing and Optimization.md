---
Date Created: 10/14/26
Kind: Lecture
Domain: Data Science
Last Updated: 10/14/26
State: "5"
Action: Study
---
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
