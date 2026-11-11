# Day 1

__Function__: code that takes in some inputs (arguments) and calculates a (return) value
>*Functions organize code, make it more testable, and can reduce the overall amount of code that needs to be written*

## Parts of a Function Definition
```python
def add_two(my_number):
  # Adds two to the argument.
  return my_number + 2
```

* __def add_two(mynumber)__: indicates we're defining the add_two function, and that it should take a single argument my_number.  (This line is called the function "header.")
	* It's typical to add a comment after the function header that describes what the function does.
* The lines that follow are indented and do some computation with the arguments.
* The instruction "return (value)" defines what the function will evaluate to when it is called.

### Variations of Functions
#### No Argument, No Return Value
Return a value of None
#### Multiple Return Values
>*The return statement should separate the different return values with commas, and where the function is called, comma-separated variables can have these multiple values assigned to them (The program thinks of them as tuples)*

# Day 2
## Scope and Local Variables

__Local Variables__: variables created within a function
	Local variables get cleaned up and become no longer accessible after the function runs

__Encapsulation__: The principle that the user of a function shouldn't need to know how it was implemented

## Shadowing

__Shadowing__: Occurs when a variable declared within a certain scope (decision block, method, or inner class) has the same name as one outside it

```python
def add_two(my_number):
  a = my_number + 2 # Shadows outer "a", now we have two a's and see this one
  print("a is " + str(a) + " inside add_two")
  return a

a = 5
print("add_two(2) is " + str(add_two(2)))
print("a is " + str(a) + " outside add_two")
```

## Refactoring

__Refactoring__: The act of trying to clean up the breakdown of the code into functions

## Pseudocode

__Pseudocode__: Code written in a style closer to English than any other particular programming language

## Comment Conventions

>*Function comments...use three double-quotes surrounding a multiline string*

```python
def get_first_letter(word):
  """ Returns the first letter of a string.

  word (str):  The string to get the letter from.

  A simple function just for demo purposes.  Probably
  not useful since get_first_letter takes more characters
  to type than string[0].
  """

  return word[0]
```
