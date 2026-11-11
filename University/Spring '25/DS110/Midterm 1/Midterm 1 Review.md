## Lecture Objectives
### Goals
__Lecture 2: Hello World and Expressions__:
- [x] Know terminology:
	- [x] expressions
	- [x] statements
	- [x] operands
- [x] Be able to follow basic programs
- [x] Know differences between types:
	- [x] str
	- [x] int
	- [x] float
	- [x] boolean

__Lecture 3: Variables and Conditions__:
- [x] Be able to follow code that assigns to variables
- [x] Be able to write conditions with <, <=, \==, >=, >, !=
- [x] Be able to follow and write:
	- [x] if
	- [x] elif
	- [x] else

__Lecture 4: While and Lists__:
- [x] While loops:
	- [x] Be able to follow flow of a program with a while loop
	- [x] Know when it's the right loop for the job
- [x] Lists:
	- [x] Be able to initialize an empty list
	- [x] Be able to access list with:
		- [x] Array notation
		- [x] Zero indexing (lst\[0])
	- [x] Know how to use list essentials:
		- [x] Append
		- [x] +
		- [x] len()
		- [x] sort()
	- [ ] Know that assigning a list assigns a reference to the same list

__Lecture 5: More Power__:
- [x] Know truth conditions of the boolean operators:
	- [x] and
	- [x] or
	- [x] not
- [x] Know how to import modules with import
- [x] Know how to use print to debug

__Lectures 6-7: Iteration__:
- [x] Be able to follow the execution of a standard for loop on a list (or other "iterable")
- [x] Be able to design a for loop that builds an answer from the input
- [x] Tuples:
	- [x] Know they're immutable (not changed after creation)
	- [x] Know they usually describe different aspects of the same thing
	- [x] Use () to create but \[] to access at index
	- [x] Iteration over tuples
- [x] Use of range() to generate numbers
- [x] Recognize break
- [x] Be able to predict the results of a nested loop and use one if necessary
- [x] Be able to read list comprehensions

__Lectures 8-9: Functions__:
- [x] Be able to write a function, given arguments and desired result
- [x] Know having no return is legal (returns None)
- [x] Understand scope of local variables in functions
- [x] Know refactoring
- [x] Know pseudocode

__Lecture 10: Dictionaries and Sets__:
- [x] Be able to write code that stores and retrieves keys/values in dictionaries and sets
- [x] Know the purpose of a hash function and roughly how it spreads out values in memory
- [x] Have at least one strategy for iterating over dictionary keys

__Lectures 11-12: numpy and matplotlib__:
- [x] Know differences between lists and arrays
- [x] Be able to create arrays from lists or lists-of-lists
- [x] Be able to use the .shape attribute
- [x] Know what broadcasting is, be able to recognize what it does
- [x] Understand slicing in code
- [x] Be able to use plt.plot()

__Lecture 13: Bigger Programs__:
- [x] Know the general strategy suggested by this lecture:
	- [x] Pseudocode
	- [x] Top-down
	- [x] Test
	- [x] Work back up
- [x] Be able to write a function that is longer than a few lines

### Responses
__Lecture 2__:
- Expression: A statement that evaluates to something
- Statement: A line of code
- Operands: The parts of code that an operator "operates" on

- str: string
- int: integer
- float: float (decimal point)
- boolean: boolean (true/false)

__Lecture 3__:

__Lecture 4__:
- append(): takes in a list argument and appends it to the list in question (list.append(appending_list))
- +: combines two lists together as one (list1 + list 2)
- len(): returns the length of a list as an int (len(list))
- sort(): returns the length of a list based the (optional) arguments reverse (defaulted to false) and key (defaulted to length/value)

__Lecture 5__:
- and: both conditions must be true, otherwise it evaluates to false
- or: either condition can be true to evaluate to true
- not: evaluates the opposite (true-false, false-true)
- importing modules is as simple as:
	- import *module_name*
	- import *module_name* as *module_name_abbreviation*
	- from *module_name* import *module_specific* as *module_specific_abbreviation*

__Lectures 6-7__:
- range(): creates a list of elements from a to b-1, or from zero up to b, with an additional (optional) argument defining the difference between values (defaults to 1)
	- range(1, 4): \[1, 2, 3]
	- range(4): \[0, 1, 2, 3]
	- range(0, 4, 2): \[0, 2]
- break: ends a for/while loop when it is reached
- list comprehension:
	- \[(statement with variable a) for a in list if (condition)]

__Lectures 8-9__:

__Lecture 10__:
- Dictionaries: use curly bracket notation, store keys that return specific values
	- {key: value, ....}
- Set: Similar to dictionaries, except they only store keys, no values
	- {key,...}
- Hash functions are used to create hash tables: they are supposed to be optimized to reduce collisions, which is when two items return the same value from a hash function
- for iteration over dictionary keys, use:
	- for *key*, *value* in mydict.items():

__Lectures 11-12__:
- Arrays can only have a single type of data, unlike lists, and arrays are limited in size once created
- Arrays are made by:
	- np.arr\[]
	- np.zeros(n) makes an array with *n* zeros
	- np.zeroes((a,b)) makes a matrix *n * n*
- *array.shape* is a tuple containing the dimensions of an array
- Broadcasting is about vectorizing operations between arrays and numbers
- Slicing uses \[a:b], where *a* and *b* are the start and end points, respectively, for which to slice