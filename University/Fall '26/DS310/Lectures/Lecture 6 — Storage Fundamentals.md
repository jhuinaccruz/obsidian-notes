---
Date Created: 10/13/26
Kind: Lecture
Domain: Data Science
Last Updated: 10/13/26
State: "5"
Action: Study
---
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
			- ==🔵$\text{offset}_0$ is metadata offsets ($1 + $ number of metadata columns)

>*We will make the following assumptions about data in the rest of the lecture*
>- *Rach character is stored using 1 byte*
>- *Integer data values are stored using 4 bytes – up to 4 billion*
>- *Integer metadata (e.g., offsets) are stored using 2 bytes – up to 65k*