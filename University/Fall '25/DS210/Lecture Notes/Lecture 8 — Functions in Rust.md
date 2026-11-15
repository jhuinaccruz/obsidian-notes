__Expression__: Simplify to a value

__Statement__: Does something without simplifying to a value

__The ways of passing parameters is through__:
- Copying (default for basic scalar types)
- Ownership (default for String and other complex types)
- __Borrowing__, or viewing it without owning it (through the use of the ampersand `&`)

__Good Functions__: Serve a single purpose (single-line functions) or clearly separate concerns (through control flow)

__Pure Function__: No side effects

__Side Effect__: Additional results or actions besides what is returned

__Validation Function__: Return a boolean through comparison

__Conversion Function__: Convert a value to another

__Helper Function__: Help clean up another part of another function or block of code

__Rust Function Naming Guidelines__:
- snake_case
- Descriptive names for variables
- Verb phrases for functions that do something
- Predicate phrases for functions that return booleans
