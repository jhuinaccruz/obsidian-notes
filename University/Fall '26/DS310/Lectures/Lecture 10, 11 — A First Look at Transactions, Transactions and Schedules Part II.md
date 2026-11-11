---
Created: 10/14/26
Kind: Lecture
Domain: Data Science
Last Updated: 10/14/26
State: "6"
Action: Study
---
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