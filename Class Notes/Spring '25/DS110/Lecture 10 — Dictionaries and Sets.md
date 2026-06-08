## Dictionaries

>*Dictionaries are common and useful in Python for organizing stored data. They let you look up a value using a string instead of a number*

__Key__: The string used to look up an item

__Value__: The item retrieved

## Hash Tables

>*Dictionaries are fast because they use a technique called hashing to ensure they're fast.*

__Hash function__: Designed specially to send data to an address within a range seemingly at random, and to spread the data evenly over the space allocated to the hash table.

>[!question]
>*What might this hash function look like?*

>[!check]
>*One approach for a string could be to convert it to a number M, then compute M^n % p for some large numbers p and n*

__Collision__: Occurs when multiple pieces of data try to go to the same place

>*if there is a collision...Python typically tried again with another, similar hash function. It can keep doing this with new hash functions until there's an open space or it realizes it's out of space*

>*...a very full hash table might run more slowly because of collisions*

## Sets

>*Sometimes there are no key-value relationships to remember...This is a good application for sets*

__Set__: Store keys using hash tables

## In

__In__:
- Works for dictionaries, sets and lists as a "getter" function
	- For sets and dictionaries: Quick hash function
	- For lists: Scans for an item

## immutability

__Immutable__: An object that once created, cannot be changed without creating a new value

>*Immutable types include strings, numbers, and tuples*

## Pass by Reference

>*...lists, dictionaries, and sets are stored by reference, so assigning one to another variable actually just assigns the reference, and the two references now point to the same place*

