__Mutating Join__: Combines variables from two data frames by matching observations by their keys, then adds the non-matching joins
- __Left/Right__ (Outer) __Joins__: Unmatched left/right columns get `null` values
	- __Full Outer Joins__: Unmatched left and right columns get `null` values
- __Inner Join__ (Conditional Join): Join occurs at a certain condition being met

__Filtering Join__: Filters the rows in a dataframe based on matches in another, without merging the tables together
- __Semi-Join__: Keeps all rows in one that have a match on the other
- __Anti-Join__: Return all rows that do not have a match in the other

__Equi Join__: Joins based on the rows matching primary key(s) in each rows respectively
- Mutating + Filtering Joins
	- Left/Right/Full Outer Joins
	- Inner Join
	- Semi-Join
	- Anti-Join

__Cross Join__ (Cartesian Product): Every row in a dataframe is matched with every row of another dataframe

__Rolling Join__: